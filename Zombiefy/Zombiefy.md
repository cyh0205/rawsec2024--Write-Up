# Zombiefy CTF Writeup

## Challenge Information
- **Category**: Steganography  
- **Points**: 400

## Objective
The objective of this challenge is to perform Steganography on a raw file. 

## Solution
After downloading and viewing the raw file, we can see it is some sort of encoded message (looks like a base something to me). 

![kowai](https://github.com/cyh0205/rawsec2024--Write-Up/assets/92976242/6d0a9c5c-0b6c-43d0-87a9-2903ab3b0c55)


So I head over to CyberChef (a great tool for decrypting) to see what I can do with it. I ended up getting an image by removing the whitespace, applying base32, and rendering the image.

![cyberchef](https://github.com/cyh0205/rawsec2024--Write-Up/assets/92976242/654d6afd-70c5-40d9-a1e5-0141ea2d1d8e)

After trying for many hours without getting anything, the organizer has released hints that lead me to two GitHub tools
- **jdvrif**: https://github.com/CleasbyCode/jdvrif
- **AudioStego**: https://github.com/danielcardeenas/AudioStego

By using the first tool, I can retrieve a mp3 file. From there, I used the second tool to retrieve a hex code. Then I decode it which returns the flag.

## Flag

![flag](https://github.com/cyh0205/rawsec2024--Write-Up/assets/92976242/b77135fb-0416-4a7c-8b6e-c3a2164129a3)

RWSC{kur0n3k0}
