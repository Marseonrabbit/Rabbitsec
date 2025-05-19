## What is internet?
---
The nuts and bolts description of the internet is the workstations and servers that holds and transit the information such as web pages and email messages and all these devices are called hosts or end devices.

---
### End-User Networks:
---
These are the networks where users access the internet from:

- **Mobile Network:** Includes smartphones, cars with internet, and other wireless devices that connect via cellular towers.
    
- **Home Network:** Consists of devices like laptops, desktops, and smart appliances connected to the internet via Wi-Fi routers.
    
- **Enterprise Network:** Used in businesses and offices, comprising multiple computers, phones, and servers connected through internal networking equipment.
### Local or Regional ISP (Internet Service Provider):
---
- These ISPs serve as intermediaries between the end-user networks and larger backbone networks.
    
- Home, mobile, and enterprise networks connect to the internet through local or regional ISPs.
### National or Global ISP:
---
- These ISPs operate on a larger scale, managing extensive backbone infrastructures and interconnecting regional ISPs.
    
- They maintain high-capacity connections across cities, countries, or globally.
### Data Center Network:
---
- Contains large-scale servers and infrastructure to store and manage data.
    
- Supports services like cloud computing, web hosting, and storage.
### Content Provider Network:
---
- Operated by companies like Google, Netflix, Facebook, etc., who serve content directly to users.
    
- These networks are optimized to deliver high-volume content (like video or social media data) efficiently.
### Interconnections:
---
- All these networks are interconnected through various routers and switches.
    
- ISPs peer with one another and connect to data centers and content networks to allow data flow across the internet.

---
- All the systems are connected with communication links and packet switches which are made up different types of physical media including cables and radio.
- So with the transmission rate of a link measure in bits per second.
- when one system send information to the another system that is called packet.
- A switch takes a packet and send them to the communication links and  in today’s Internet are routers and link-layer switches. Both types of switches forward packets toward their ultimate destinations. Link-layer switches are typically used in access networks, while routers are typically used in the network core. The sequence of communication links and packet switches traversed by a packet from the sending end system to the receiving end system is known as a route or path through the network. 
---
**So in a simple way**:
Imagine sending a text from your phone to your friend's phone:

1. Your phone breaks the message into packets.
    
2. Those packets go to your **Wi-Fi router** (a packet switch).
    
3. The router sends them to your **local ISP**.
    
4. They pass through **many routers** (each choosing the next step).
    
5. The packets reach your friend's phone, and it reassembles them into the full message.
---
Imagine you have a large package (your data) to send from your house (the sending end system) to a friend's house far away (the receiving end system)

- instead of sending the whole package as one big piece, you break it down into smaller boxes (packets).
  
- You load these boxes onto a fleet of trucks.
  
- Each truck travels independently through a network of roads and highways (communication links).
  
- At intersections (packet switches, like routers), someone (the switch/router) looks at the address on each box and decides which road the truck should take next to get closer to the destination. Routers use information in the packet's header for forwarding.
  
- When all the trucks arrive at your friend's house, the boxes are unloaded and put back together to form the original large package.

So, it's like a delivery system where data is broken into small, independently routed pieces (packets) that travel over shared pathways (links) through directing points (switches/routers) and are reassembled at the end.

---
End systems, packet switches, and other pieces of the Internet run protocols that control the sending and receiving of information within the Internet. The **Transmission Control Protocol (TCP)** and the **Internet Protocol (IP)** are two of the most important protocols in the Internet.

---
### Why Protocols and Standards Matter on the Internet:

The **Internet only works smoothly** because everyone agrees on how things should communicate — like speaking the same "language."

---
### What are Protocols?

**Protocols** are the **rules** that computers follow to talk to each other — for example:

- **TCP/IP**: Sends data reliably.
    
- **HTTP**: Loads websites.
    
- **SMTP**: Sends emails.
---
### Who Makes the Rules?

The **Internet Engineering Task Force (IETF)** creates these rules (protocols) and writes them in documents called [**RFCs**](https://www.ietf.org/rfc/) (Requests for Comments).

- [**RFCs**](https://www.ietf.org/rfc/rfc-index.txt) are detailed, technical documents that explain exactly how a protocol works.
    
- Despite the name, RFCs are official and important — like instruction manuals for building the internet.
---

### What About Hardware?

For things like Wi-Fi or Ethernet (how your computer connects to the internet), other groups like [**IEEE 802**](https://www.ieee802.org/) make the rules.

---
### Summary:

- The internet works because **everyone follows the same standards**.
    
- These standards are written in [**RFCs by IETF**](https://www.ietf.org/rfc/).
    
- **IEEE** writes standards for physical connections like Wi-Fi and Ethernet.

Now let's talk about the 
1. Chapter 1 [[COMPUTER NETWORKS AND THE INTERNET]]
2. 
