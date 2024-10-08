# Tor-exit-node-guide
---
###  What is Tor
Tor is a network of virtual tunnels that allows you to improve your privacy and security on the Internet. Tor works by sending your traffic through three random servers (also known as relays) in the Tor network. The last relay in the circuit (the "exit relay") then sends the traffic out onto the public Internet.

### What is Tor Browser
Tor Browser uses the Tor network to protect your privacy and anonymity

### Exit Nodes
The exit node is where your web traffic exits the Tor network and is directed to its final destination. Tor Browser typically selects exit nodes randomly for internet browsing. However, there are scenarios where using specific exit nodes is necessary such as for testing, research, or accessing content from a particular country or region.<br>
**The exit node cannot view your IP address but can identify the site it is connecting to.**

### Torrc Configuration File
The core Tor configuration file is called torrc, It can be found at <br>
<br> **Windows**:  C:\Users\<YourUsername>\AppData\Roaming\Tor\torrc <br>
**macOS/Linux**:  /etc/tor/torrc or ~/.tor/torrc <br>
<br >If you changed the installation directory when installing then check the directory where you installed it

### Modifying
To Modify the torrc, just add the lines :<br>
![Tor Configuration File](eg1.png) <br>
Replace `{ua}` with Country of your choice <br>

<br> **StrictNodes 0** - Tor will prefer to use the specified nodes but will connect to others if necessary to maintain the connection.
<br>
**StrictNodes 1** -This means Tor will not connect to any nodes outside the ones specified. <br>

<br> ![Tor Configuration File](eg2.png) <br>
You can also add multiple Countries by placing them after a comma.<br>

<br> ![Tor Configuration File](eg3.png) <br>
If you have a specific IP Address for exit node then you can use it in the same manner. <br>

### Blacklisting
You can also use this as a security measure by configuring Tor to completely avoid certain exit nodes. <br>
<br> ![Tor Configuration File](eg4.png) <br>
Exclude the mentioned Country Code from using as Exit Node <br>
<br> ![Tor File](eg5.png) <br>
Exclude the mentioned Country Codes from using as any kind of Nodes <br>

---
### For References
Check [References.md](References.md).
