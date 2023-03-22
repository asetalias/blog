Hi everyone, This blog explores the new communication protocol, known as Matter which is being developed by <strong>Connectivity Standards Alliance (CSA)</strong>
<br>
To know more, Let's go on a journey and explore the new generation of communication protocols.
<br>

  ## What's Matter?
  As the IoT market boomed. The popularity for smart home devices shot up. This resulted in a new market of Smart Home. Many companies joined hands and contributed to this boom by making Smart Devices.
  As there were a large number of devices, our general communication protocols such as Wifi, Bluetooth couldn't keep up. To provide a solution for this new protocols like Z-wave, emerged. But overtime they were also hit by the demand.
  This resulted in a huge wave of devices each having a different communication protocol, and requiring a hub to function.
  With time, a new revolution was long overdue. Google joined hands with Amazon, Apple, Zigbee Alliance together forming a new group known as CSA. To revolutionize the communication protocol.
  They sought to develop a unified solution. All the major companies that we know today, joined hands in this journey to build a unified solution for IoT devices.
  This was known as Project CHIP( COnnected Home Over IP). It evolved into what we know today as Matter.
  </p>
  
  ## Why Matter should matter?
  <p> As a consumer, Why should I even bother with Matter?. This was the question that was raised when Project CHIP was revealed in December 2019.
  Matter aims to unify all the communication standards that we know today, by using compatible smart home devices.
  But this option of switiching will be very expensive for me. Matter solves this problem by being compatible with current generation of smart home devices such as Google   Home, Nest, Amazon Echo, Apple Homekit.
  <br>
   As a device developer <b>Matter</b>, makes it easier for us to integrate one protocol and thus simplifies the development and increases compatibility for the users. Matter machines enables local communicationbetween smart home devices, mobile apps and also provides communication with cloud services by defining a set of IP-based Networking technologies for device certification.
  <br>
  As a consumer, <b>Matter</b>, makes my mind comfortable that, the device will work with my current smart home standards, and everything can be controlled from one place, this allows me to use to many devices with little to no overheads and provides an easy to use experience.
  <br>
 </p>
 
 ## Architecture overiew 
   
<p>
   Matter aims to build a universal IPv6- based communication protocol for smart home devices. The protocol defines the application layer that will be deployed on devices and the different link layers to help maintain interoperability.
   
   The Matter architecture is divided into layers to seperate different responsibilities and introduce a good level of encapsulation among the various pieces of the protocol stack. Following describes each layer and their role in the protocol stack.
   <br>
   1. <b>Application</b>: This layer is focused on the application part of the device. It deals with High-order business logic of a device. For eg. A light bulb to turn on/off.
   2. <b>Data Model</b>: The data layer corresponds to the data and verb elements that helps to support the functionality of an application. It operates on these data structures when there is an intent to interact with the device.
   3. <b>Interaction Model</b>: The interaction Model layer defines a set of interactions that can be performed between a client and a server device. For example, reading or writing attributes on a server device would correspond to application behavior on the device. These interactions operate on the elements defined at the data model layer.
   4. <b>Action Framing</b>: Once an action is constructed by using the interaction model, it is serialised in a binary format to encode for Network Transmission.
   5. <b>Security</b>: An encoded action frame is then sent down to the Security Layer to encrypt and sign the payload to ensure that data is secured and authenticated by both sender and reciever of a packet. Also  by being based upon the IPv6 protocol offers security features and makes it impossible for address scanning.
   6. <b>Message Framing and Routing</b>: With an interaction encrypted and signed, the Message Layer constructs the payload format with required and optional header fields.
   7. <b>IP Framing and Transport Management</b>: After the final payload has been constructed, it is sent ot the underlying transport protocol for IP management of the data.
</p>
<br>
## Development Goals of Matter
<br>
<p>
  Currently Matter is being developed with the following goald and principles in mind:
  1. <b> Unifying </b>: Matter is built with and on top of market-tested technologies.
  2. <b> Interoperable</b>: The specification permits communication between any Matter-certified device.
  3. <b> Secure</b>: The Specification leverages modern security practices and protocols.
  4. <b> User Control</b>: The end user controls authorization for interaction with devices.
  5. <b> Federated: No single entity serves as a throttle or a single point of faulure for root of trust.
  6. <b> Robust</b> The set of protocols aims to provide a seamless out of box experience for it's users.
  7. <b> Open</b>: The project's design and technical processes are open and transparent to the general public, including non members wherever possible.
  </p>
  
  
  

  
