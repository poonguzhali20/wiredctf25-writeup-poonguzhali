# VINtercept(AUTOMOTIVE):
     1.Basically this challenge comes under automotive. I need to get VIN(Vehicle Identification number) id to complete this   task.This challenge tests our ability to interact with in-vehicle network.So all I have to do is extract the VIN from a vehicle system using UDS(Unified diagnostic Service) over can. 
     2.An ECU(ELECTRONIC CONTROL UNIT) hardware was given. It is basically the computer inside a vehicle that controls specific functions and I communicated to it through CAN bus. CAN bus is controller Area Network that allows different part of vehicle like ECU to talk to each other. "ECU replies in 0*73B" this is the hint I was given. It means the replying can id is 0*73B , so I had to find requesting can id through this, only then my requests will be sent to ECU. 
     3.Here UDS allows us to request information. After identifying the correct CAN ID to send the request which is 0*733, I used the UDS command to request the VIN. The task involves a Raspberry Pi with CAN capabilities to interact with ECU and retrieve the VIN.To begin, "sudo apt update , sudo apt install can-utils", I used these these commands in linux terminal to install it.
     4.Before using these can commands, I was supposed to configure and bring up the CAN interface. "sudo ip link set vcan0 type can bitrate 500000", "sudo ip link set up vcan0", used these these commands to set the bitrate and to bring the interface up. To monitor CAN traffic and send messages at the same time , I used a tmux session, I split the terminal into horizontally using ctrl+b+", tmux command. 
     5.I navigated between panes using ctrl+b then arrow keys."can send vcan0 733#0322F1900000", crafted this UDS request to get the vin using service 0*22 standard for VIN,here 733 = ECU request id.  
     6.After that I requested for full vin id using "cansend vcan0 733#300000000000", In the candump pane, I received a response which had VIN id in hexadecimal form, after decoding it to ascii using online decoder I finally got the VIN which is the flag for this challenge.

## TOOLS USED:
    >Can-utils
    >tmux shortcuts
    >rasperry Pi
