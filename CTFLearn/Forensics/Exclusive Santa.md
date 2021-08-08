Extract hidden file by binwalk,

```powershell
PS H:\CTF\CTFLearn> binwalk.bat --dd='.*' .\3.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 1200 x 875, 8-bit/color RGBA, non-interlaced
78            0x4E            Zlib compressed data, default compression
52406         0xCCB6          PNG image, 1280 x 720, 8-bit/color RGBA, non-interlaced
52447         0xCCDF          Zlib compressed data, compressed
```

On image 3.png, that's hint for combination image, use stegsolve open 3.png then Analyse -> Image Combiner, select image we just extract

![image](https://user-images.githubusercontent.com/58476264/128620350-9ed601f8-b389-482b-90a2-2bc0eaa50ddc.png)

A new windows is displayed, we see the flag

![flag](https://user-images.githubusercontent.com/58476264/128620376-4594d261-ec8e-4e83-89be-dda980316f9c.png)

Flag: **CTFLearn{Santa_1s_C0ming}**
