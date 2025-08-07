# ATtention_ESP(Embedded)
     This was an embedded system CTF challenge. An ESP32 DEV module was connected to my system and I had to retrieve the flag using AT commands
    1."AT" used this command to check communication
    2."AT+GMR" to check version , the version was shown after this and the first part of flag was released, which is wired{
    3."AT+CWLAP" to list available networks and the second part of the flag was released, C0nn3
    4."AT+CWJAP="CONNECT_ME","12345678" to connect to a network and third part of the flag was released , which is c7ed_
    5."AT+CIFSR" to get IP address and fourth part of the flag is 0v3r_
    6."AT" to end confirmation and final part of the flag is AT}
    7.So the flag is wired{C0nn3c7ed_0v3r_AT}
## TOOLS USED
    >ESP32 module
    >AT firmware that enables AT command support on ESP32
