Extract resource: receive lots of directories having name only a character<br>
![image](https://user-images.githubusercontent.com/58476264/129221425-73dee6d9-113b-45d0-880a-bf107895a582.png)

In some directories, it contains some file with name is a number<br>
![image](https://user-images.githubusercontent.com/58476264/129221466-08f4c41f-e27e-40c2-aa94-75fded5df2f7.png)

When we sort with name of directories, then receive a string
SFRCe0RJUjNjdEx5XzFuX1BsNDFuX1NpN2V9
This is a base64 string, decode it
```powershell
>>> import base64
>>> base64.b64decode('SFRCe0RJUjNjdEx5XzFuX1BsNDFuX1NpN2V9')
b'HTB{DIR3ctLy_1n_Pl41n_Si7e}'
```

Flag: **HTB{DIR3ctLy_1n_Pl41n_Si7e}**
