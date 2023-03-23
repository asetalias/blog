+++
title = 'Matter and the future'
slug = 'Matter_future'
image = '/static/images/Cover.jpeg'
date = "2023-03-23T10:00:00"
author = 'Tushar Bhatia'
tags=['IoT', 'Networking', 'Smart Home', 'Smart Devices', 'Google-projects']
categories =['IoT', 'Smart-Devices', 'Smart Homes', 'Networks']
description = 'This blog explores Matter a new communication protocol made by CSA'
disableComments = false
+++

Hi everyone, This blog explores the new communication protocol, known as Matter which is being developed by <strong>Connectivity Standards Alliance (CSA)</strong>
<br>
To know more, Let's go on a journey and explore the new generation of communication protocols.
<br>

  ## What's Matter?
  As the IoT market boomed. The popularity of smart home devices shot up. This resulted in a new market for Smart Home. Many companies joined hands and contributed to this boom by making Smart Devices.
  <br>
  <br>
  As there were a large number of devices, our general communication protocols such as Wifi and Bluetooth couldn't keep up. To provide a solution for this new protocols like Z-wave, emerged. But over time, they were also hit by the demand.
  This resulted in a huge wave of devices each having a different communication protocol, and requiring a hub to function.
  With time, a new revolution was long overdue. Google joined hands with Amazon, Apple, and Zigbee Alliance together forming a new group known as CSA. To revolutionize the communication protocol.
  <br>
  <br>
  They sought to develop a unified solution. All the major companies that we know today, joined hands in this journey to build a unified solution for IoT devices.
  This was known as <b>Project CHIP( Connected Home Over IP)</b>. It evolved into what we know today as <b>Matter</b>.
  </p>
  
  ## Why Matter should matter?
  <p> As a consumer, Why should I even bother with Matter? This was the question that was raised when Project CHIP was revealed in December 2019.
  Matter aims to unify all the communication standards that we know today, by using compatible smart home devices.
  But this option of switching will be very expensive for me. Matter solves this problem by being compatible with the current generation of smart home devices such as Google   Home, Nest, Amazon Echo, and Apple Homekit.
  <br>
  <br>
   As a device developer <b>Matter</b>, makes it easier for us to integrate one protocol and thus simplifies the development and increases compatibility for the users. Matter machines enable local communication between smart home devices, and mobile apps and also provide communication with cloud services by defining a set of IP-based Networking technologies for device certification.
  <br>
  <br>
  As a consumer, <b>Matter</b>, makes my mind comfortable that, the device will work with my current smart home standards, and everything can be controlled from one place, this allows me to use many devices with little to no overheads and provides an easy to use experience.
  <br>
 </p>
 
 
 ## Architecture Overview 
![image](https://github.com/Tushar-Bhatia-21/blog/blob/master/static/images/Matter_Layered_Arch-min-min.jpeg#center)
<p>
  
   Matter aims to build a universal IPv6- based communication protocol for smart home devices. The protocol defines the application layer that will be deployed on devices and the different link layers to help maintain interoperability.
   
   The Matter architecture is divided into layers to separate different responsibilities and introduce a good level of encapsulation among the various pieces of the protocol stack. The Following describes each layer and their role in the protocol stack.
   <br>
   1. <b>Application</b>: This layer is focused on the application part of the device. It deals with the High-order business logic of a device. For eg. A light bulb to turn on/off.
   2. <b>Data Model</b>: The data layer corresponds to the data and verb elements that help to support the functionality of an application. It operates on these data structures when there is an intent to interact with the device.
   3. <b>Interaction Model</b>: The interaction Model layer defines a set of interactions that can be performed between a client and a server device. For example, reading or writing attributes on a server device would correspond to application behavior on the device. These interactions operate on the elements defined at the data model layer.
   4. <b>Action Framing</b>: Once an action is constructed by using the interaction model, it is serialized in a binary format to encode for Network Transmission.
   5. <b>Security</b>: An encoded action frame is then sent down to the Security Layer to encrypt and sign the payload to ensure that data is secured and authenticated by both sender and receiver of a packet. Also being based upon the IPv6 protocol offers security features and makes it impossible for address scanning.
   6. <b>Message Framing and Routing</b>: With an interaction encrypted and signed, the Message Layer constructs the payload format with required and optional header fields.
   7. <b>IP Framing and Transport Management</b>: After the final payload has been constructed, it is sent to the underlying transport protocol for IP management of the data.
</p>


## Development Goals of Matter
<p>
Currently, Matter is being developed with the following goals and principles in mind:<br>
  1. <b> Unifying </b>: Matter is built with and on top of market-tested technologies.<br>
  2. <b> Interoperable</b>: The specification permits communication between any Matter-certified device.<br>
  3. <b> Secure</b>: The Specification leverages modern security practices and protocols.<br>
  4. <b> User Control</b>: The end user controls authorization for interaction with devices.<br>
  5. <b> Federated</b>: No single entity serves as a throttle or a single point of failure for root of trust.<br>
  6. <b> Robust</b> The set of protocols aims to provide a seamless out of box experience for its users.<br>
  7. <b> Open</b>: The project's design and technical processes are open and transparent to the general public, including non-members wherever possible.<br>
    </p>
  <br>
  
  <b> Matter</b> does seem to be a very important part of the future. As we all know, it is the thirst of a human being for knowledge. So let's see how <b> Matter </b> works in a smart home environment.
  
  ## How does it work?
  ![image](https://github.com/Tushar-Bhatia-21/blog/blob/master/static/images/Thread_Matter.jpeg#center)
 <p>
  Let's see how a packet would be sent from the <b> Matter Controller</b> to the Matter-enabled device, over the <b>Matter Protocol</b>.
  Let's take an example of a nest hub as a matter-enabled hub and a light device.<br>
  <br>
  1.<b> Creating a packet</b>: As we want to connect with the light device. A Smart Packet is made and is encrypted in a string of 0's and 1's. This smart packet contains information about the data being transmitted and information about the data being in the device.
  <br>
  <br>
  When the device sends a packet, the application layer prepares the packet for transmission by adding any necessary application-level data.<br>
  <br>
  2.<b> Routing the Smart Packet</b>: The light then sends the smart packet to the Google Nest Hub router using the thread protocol. As thread uses IPv6 protocol, it can directly connect to the internet and enables a low latency transmission. Here a header and trailer are also added. A header contains information about the sender and receiver and information about the packet's sequence number and other parameters. The trailer contains information that enables the receiving device to detect any errors that may occur in transmission.
  <br>
  <br>
  This occurs over the network layer, the network layer also determines the optimal path for the packet to reach its destination.<br>
  <br>
  3.<b> Decrypting and Parsing the Smart Packet</b>: The Google Nest Hub router then receives the smart packet and decrypts the string of 0 and 1's using the Matter Protocol. The router then parses the packet to extract the data and information about the sender.
  <br>
  <br>
  This occurs over the link layer. The link layer is responsible for managing the physical layer of the communication. It is responsible for sending and receiving packets over the air using the Thread Wireless protocol. The link layer modulates the digital data into an analog signal that can be transmitted over the air using Radio Waves.<br>
  <br>
  4. <b>Forwading the Data</b>: The Google Nest hub router then forwards the data contained in the smart packet to the appropriate given device in the Smart Home Environment. This occurs over the Physical Layer, As it is responsible for transmitting the modulated signal over the air using radio waves. When a device sends a packet, the physical layer then transmits the modulated signal over the air to the receiving device.<br>
  <br>
  <br>
  5. <b>Acknowledging the Command</b>: Once the command is executed and received by the Smart Light it will send a response packet back to the device that originally send the smart packet to confirm that the command was executed successfully.
  <br>
  <br>
  The Same Response packet is sent over the same layers and thus the response packet is confirmed by the Nest Hub, this shows that the command has executed successfully.
<br>
We have now seen how a packet is sent and received over a Smart Home Network. Let's continue towards the Next Leg of our Journey and explore the Future with Matter. 
</p>
 
## Future of Matter
![image](https://github.com/Tushar-Bhatia-21/blog/blob/master/static/images/CSA%20Matter.jpeg)
<p>
  The current status of Matter involves an Open-Source Approach. The design and technical processes are intended to be transparent to the public, including to Working Group non-members wherever possible. Matter endeavors to bring together the best aspects of market-tested technologies and redeploy them as a unified cohesive whole-system solution. The Overall Goal of this Approach is to bring the best experience to the consumers and manufacturers as quickly as possible.
  <br>
  <br>
  Till now, in the market there are no Matter-enabled devices available, however, this is sure to change in a few months. Major Companies such as Google, Amazon, Apple, and many more have rolled out updates to make their current devices <b> Matter-ready</b>. This ensures a seamless transition to a new ecosystem automatically. In the future, we can expect new updates to the Matter Protocol itself, and the many ways Legacy Products will be supported in a Matter-Enabled Ecosystem.
  <br>
  <br>
  We all are currently in the Middle of a revolution, and if you want to be a part of this revolution.
  Check out the GitHub repositories and the links for contribution in the <b>Reference Section</b>. AliAS will soon be covering a new Blog <b> Getting Started With Matter</b>. So I will meet you, on the next Leg of our Journey. ♥
 </p>
 
 ## Reference Links
 1. https://csa-iot.org/all-solutions/matter/
 2. https://github.com/project-chip/connectedhomeip
 3. https://www.theverge.com/22832127/matter-smart-home-products-thread-wifi-explainer
 4. https://developers.home.google.com/matter
