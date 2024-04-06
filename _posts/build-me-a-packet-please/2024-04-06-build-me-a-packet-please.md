---
layout: post
title: Build me a packet please!
date: 2024-04-06 21:01 +0545
url: external
---


## Packets
    
> tl;dr: Packet is built upon the protocol it is travelling in.It goes woosh woosh with essential data and also contains its size along with its type of data. 

<img style="width:700vh;height:200px;" src="https://i.redd.it/9qapun2q95o31.jpg">

<small style="font-size:10px">This is a physical packet</small>


---
---

###  Trying to build a packet and create our own network connection with clear exchange of data.


➡️ `Protocol`:

A protocol a set of rules that a network connect should/could follow for uniformity of exchange.
So,its not necessary but is.<br>So,for now,lets us just assume a simple protocol of an arbitrary name of saltim.It's just that easy,now as we're done with the hard part.Now for the easy bit.

Some of the more commonly used protocols are:

1.`TCP(Trasmission Control Protocol)↔️`
2.`UDP(User Datagram Protocol)➡️`
3.`FTP(File Transfer Protocol)🗃️`
4.`IP(Internet Protocol)🌐`

➡️ `Designing a packet`:

So,A packet in the most fundamental state is just pure data.Anything could be a packet.It could be you throwing a ball of binary `101010100110000001001` to your friend during the class or a president hitting the button for the nuclear missile to set its way with complex set of instructions within the packet to make sure of its authenticity.

So our packet in `saltim` which is a very basic packet would kind of look like this in high-level with the payload and all the attached info along with it.The data along with will be explained in.

<img src="/assets/packet_filled_of.png">

➡️ `The packet's data architecture.`

So,from the above assumption of the saltim packet that we use.The saltim packet has the different parts to a structure in the packet:

1.`The Payload` 
   
   The payload to a data contains the important data to a packet, **essentially**,the data that is sent by the by any of the parties that are involved in the connection. 

It could be anything of the sort of saying hello,to being a bash command being sent.

> It is kind of impossible for one to decrypt what is said in the modern day encryption that is used for the packets that travel via selected protocols.

2.`Size info`

Yes,sorry guys,but *size does matter*.In case of packets,it is quite necessary for the packets to contain their size info to be attached else it is not possible to locate the end of the packet and the start of another packet as a connection has a flow of packets.A end info the packet end could be helpful to locate the end of the packet and make it easier for the location of the then packet.

3.`Info data`

A data in the payload can be a various types:`xml`,`json`,etc.
<br>
So,for the data type to be known it could be helpful for the receiver to parse the data as the data received has a known structure.

    {
        size-info:10,//assumed
        payload:"Turn On",
        end-info:0x1B39, 
        data-info:"json"    
    }

4.`End info`

The endinfo contains an end pattern that the receiver is able to identify as a pattern of ending byte.It could be anything but it must be something that isn't included in the payload data.ie.If the payload data is an ascii string anything out of the ascii range,ie,8 bit data we could make an ascii string.So,we could assume

    0x1B39

a data passed as ending sequence as it is not included in the ascii range.Since the data isn't passed in the ascii range,it packet would be considered ended and the packet read would be completely received.

> WOOOOOOOOOOOO!! The packet is ready to be sent.


## Ending note:

**It could be said that this model of implementation of packet sending and networking is only a theoritical model**
**that could be used for small implementation that are easily compromisable with various flaws and disadvantages,**
**but yet,these were the only protocols that were able to build other more complex protocols,as they're just a**
**manifestation of smaller protocols.**


[Took an understanding of this video](https://www.youtube.com/watch?v=kH7P1ZX44DQ)
