# Webserver 

so we know how on of stuff we know ho to connect with the internet lets get the ball roooling lets make a simple webserver .
i found a good tutorial on how https://randomnerdtutorials.com/esp32-esp8266-micropython-web-server/

this user has made a really goood tutorial visit his website :)

***code***
```# Complete project details at https://RandomNerdTutorials.com

try:
  import usocket as socket
except:
  import socket

from machine import Pin
import network

import esp
esp.osdebug(None)

import gc
gc.collect()

ssid = 'REPLACE_WITH_YOUR_SSID'
password = 'REPLACE_WITH_YOUR_PASSWORD'

station = network.WLAN(network.STA_IF)

station.active(True)
station.connect(ssid, password)

while station.isconnected() == False:
  pass

print('Connection successful')
print(station.ifconfig())

led = Pin(2, Pin.OUT)
```

basically

As mentioned previously, we create our web server using sockets and the Python socket API. The official documentation imports the socket library as follows:

try:
  import usocket as socket
except:
  import socket
We need to import the Pin class from the machine module to be able to interact with the GPIOs.

from machine import Pin
After importing the socket library, we need to import the network library. The network library allows us to connect the ESP32 or ESP8266 to a Wi-Fi network.

import network
The following lines turn off vendor OS debugging messages:

import esp
esp.osdebug(None)
Then, we run a garbage collector:

import gc
gc.collect()
A garbage collector is a form of automatic memory management. This is a way to reclaim memory occupied by objects that are no longer in used by the program. This is useful to save space in the flash memory.

The following variables hold your network credentials:

ssid = 'REPLACE_WITH_YOUR_SSID'
password = 'replace_with_your_password'
You should replace the words highlighted in red with your network SSID and password, so that the ESP is able to connect to your router.

Then, set the ESP32 or ESP8266 as a Wi-Fi station:

station = network.WLAN(network.STA_IF)
After that, activate the station:

station.active(True)
Finally, the ESP32/ESP8266 connects to your router using the SSID and password defined earlier:

station.connect(ssid, password)
The following statement ensures that the code doesn’t proceed while the ESP is not connected to your network.

while station.isconnected() == False:
  pass
After a successful connection, print network interface parameters like the ESP32/ESP8266 IP address – use the ifconfig() method on the station object.

print('Connection successful')
print(station.ifconfig())
Create a Pin object called led that is an output, that refers to the ESP32/ESP8266 GPIO2:

led = Pin(2, Pin.OUT)


# thats just for configuration this the main code 
```
# Complete project details at https://RandomNerdTutorials.com

def web_page():
  if led.value() == 1:
    gpio_state="ON"
  else:
    gpio_state="OFF"
  
  html = """<html><head> <title>ESP Web Server</title> <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="icon" href="data:,"> <style>html{font-family: Helvetica; display:inline-block; margin: 0px auto; text-align: center;}
  h1{color: #0F3376; padding: 2vh;}p{font-size: 1.5rem;}.button{display: inline-block; background-color: #e7bd3b; border: none; 
  border-radius: 4px; color: white; padding: 16px 40px; text-decoration: none; font-size: 30px; margin: 2px; cursor: pointer;}
  .button2{background-color: #4286f4;}</style></head><body> <h1>ESP Web Server</h1> 
  <p>GPIO state: <strong>""" + gpio_state + """</strong></p><p><a href="/?led=on"><button class="button">ON</button></a></p>
  <p><a href="/?led=off"><button class="button button2">OFF</button></a></p></body></html>"""
  return html

s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
s.bind(('', 80))
s.listen(5)

while True:
  conn, addr = s.accept()
  print('Got a connection from %s' % str(addr))
  request = conn.recv(1024)
  request = str(request)
  print('Content = %s' % request)
  led_on = request.find('/?led=on')
  led_off = request.find('/?led=off')
  if led_on == 6:
    print('LED ON')
    led.value(1)
  if led_off == 6:
    print('LED OFF')
    led.value(0)
  response = web_page()
  conn.send('HTTP/1.1 200 OK\n')
  conn.send('Content-Type: text/html\n')
  conn.send('Connection: close\n\n')
  conn.sendall(response)
  conn.close()
  ```