Open image and pay attention to the red area

![forest](https://user-images.githubusercontent.com/58476264/128490552-90e8e085-2f37-4fa8-b050-0ff4a4a0680f.jpg)

Use stegsolve at Random colour map 2,

![Untitled5](https://user-images.githubusercontent.com/58476264/128493555-1b56d5fd-6d2c-4f25-99f0-aa695f8394a2.png)

Next, use steghide to extract hidden with this password
```
> .\steghide.exe extract -sf .\forest.jpg -p IsJuS1Af0r3sTbR0
wrote extracted data to "nothinghere.txt".
```

We see a string maybe the flag, decrypt with Ceasar

![Untitled6](https://user-images.githubusercontent.com/58476264/128495586-4225296d-0e9a-4ac0-bf6b-2b6bde9a26c2.png)

Flag: **HTB{AmAz1nGsKilLzZBr0}**
