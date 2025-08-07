# ESP-ionage-2.0(Embedded):
    This was an embedded embedded ctf challenge. I connected my system to espionage wifi. I used this IP: 192.168.4.1 id and    entered into page. 
    1."nothing to see here", it was shown in that page
    2.So I right clicked it and entered view page source
    3.grep -i flag 192.168.4.1/index.html, after using this command it said file not found and a hint was given as Z28gdG8gL2dob3N0.
    4.after searching it , the page showed as "only who look deeper will find what they seek".
    5.again I entered view page source in the browser and flag was in cipher text and I used decoder to get the flag.
    6.flag: wired{valar_morghulis_all_must_die}
## TOOLS USED:
    >Espionage wifi
    >grep and cat commands
    >cipher decoder
