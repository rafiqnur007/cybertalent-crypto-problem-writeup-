# cybertalent-crypto-problem-writeup-

# 1.Hash3rror
problem: we got this corrupted hash password from a Pcap file with a note (password = sha-1(hash-result)).

HASH:77be5d24ed2e3e590045e1d6o7e84i50d2799c19f48ede46804a8734e287df120f <br>

# Solution:
It's basically in hex format, right? But no, it has two illegal characters: o and i. Let's remove that. Now, it's 64 characters long, which is the length of a sha-256 hash.

We get the plaintext s3cr3tpassword. Now, as per instruction, we've to sha-1 encrypt it. After encryption, we get 83874343435092cb681c0d558a84bfeb389c32ed. That's our solution.

## 2. UP
problem: Every time you go up you will gain one ballon

ejxc{T0nY0J_BsUMS4}

# Solution: 
By hunch, we can map ejxc to flag by adding their position in the string to themselves. After mapping each alphabetic character, we get: <br> flag{Y0uG0T_MeHAH4}


# 3 Postbase
problem: We got these letters and numbers and don't understand them. Can you?

R[corrupted]BR3tCNDUzXzYxWDdZXzRSfQ==

# Solution:
The trailing == looks like a BASE64 string. Let's remove R[corrupted] part and decode it. We get G{B453_61X7Y_4R}. Now, it's common sense that the complete flag would be <br> FLAG{B453_61X7Y_4R}
