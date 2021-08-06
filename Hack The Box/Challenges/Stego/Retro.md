Use binwalk extract zip file
```powershell
PS H:\CTF\Hackthebox.eu\Stego> binwalk.bat --dd='.*' .\retro.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
28            0x1C            TIFF image data, big-endian, offset of first image directory: 8
233685        0x390D5         Zip archive data, at least v2.0 to extract, compressed size: 76, uncompressed size: 87, name: eighties_were_nice.txt
233813        0x39155         Zip archive data, at least v2.0 to extract, compressed size: 3991, uncompressed size: 549308, name: retro.wav
238038        0x3A1D6         End of Zip archive, footer length: 22

PS H:\CTF\Hackthebox.eu\Stego\_retro.jpg.extracted> unzip.exe .\390D5.zip
Archive:  .\390D5.zip
  inflating: eighties_were_nice.txt
  inflating: retro.wav

PS H:\CTF\Hackthebox.eu\Stego\_retro.jpg.extracted> cat .\eighties_were_nice.txt
Retro style is nice! I hope you can find the "flag" as we usually did in the eighties
```

Based on the hint 80's, I found the tool [MakeTZX](http://ramsoft.bbk.org.omegahg.com/maketzx.html) convert wav to tzx

![Untitled7](https://user-images.githubusercontent.com/58476264/128499122-34b723ea-8a07-4167-b31a-7eb27f9aa4ab.png)

```powershell
PS H:\CTF\Hackthebox.eu\Stego\_retro.jpg.extracted> strings.exe .\new.tzx
ZXTape!
Created with Ramsoft MakeTZX
flag
"r3tr0-1s-4l1v3"
```

Flag: **HTB{r3tr0-1s-4l1v3}**
