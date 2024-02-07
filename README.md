A packet sniffer examines streams of data flowing through computers on a network. Otherwise known as a packet analyzer; this protocol can be useful for businesses to test where they are at fault if a malicious actor wanted to insert
themselves onto the businesses network and read the data running through. 
<br>
<br>
For example I will show using Wireshark how a packet sniffer works.
<i>For the example I have used a site called [http://testphp.vulnweb.com/login.php] . Please note that this is not a real site and the packet filter only works on sites that are "Not secure". </i>
<br>
<br>
1. Open Wireshark
2. Select the network you want to use (in my case I selected Wi-Fi)
3. Once network is selected, Wireshark will automatically read the selected networks traffic
#
<br>
<ins>How to test:</ins> <br>
I recommend using a fake website called [http://testphp.vulnweb.com/login.php] to demonstrate.<br><br>
1. While having Wireshark open and reading your network, select "Signup" in the menu on the left side of the site<br>
2. Now enter in the username and password - can be anything, literally make it up, it's not a real site<br>
3. Press "login" once done
4. Now go back to Wireshark and stop the search by pressing the red square in the top left of Wiresharks menu bar
5. Now with Wireshark paused, enter in the top search bar (used to filter out attributes from the network protocols) the following:
<br>
<br>
<p align="center">http.request.method== "POST"</p>
<br>
6. Once filtered, a subbox should come up<br>
7. Select the following sub-menu:
<br>
<br>
<p align="center">HTML Form URL Encoded: appplication/x-www-form-urlencoded</p>
<br>
8. Once selected, you should be able to see the exact username and password in which you entered.
<br>
<br>
<ins>Example:</ins>

![image](https://github.com/mholtz15/PacketSniffer/assets/157908872/496d051c-3a76-48ee-a56d-ad7b0b694877)



