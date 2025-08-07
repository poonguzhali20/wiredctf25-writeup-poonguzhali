# 1_that_replied(Wireless):
    1.A wireless ctf challenge. 
    2."We've intercepted a network capture from a suspicious machine that was communicating with a local web server." is the
      the description of the challenge
    3.And a file was given with extension .pcab, to access that file , I installed wireshark.
    4."looks like meaningless noise repeated HTTP requests to random pages that don’t even exist.", I considered it as hint 
      which was given in the description.
    5."wireshark -r captured.pcab" to open a file in wireshark
    6.After opening it in wireshark, I found something different in base64
    7.I decoded it using base64 decoder and that is the flag
    
## TOOLS USED:
    >wireshark
    >base64 decoder.
