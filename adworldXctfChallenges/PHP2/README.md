# Challenge: https://adworld.xctf.org.cn/task/answer?type=web&number=3&grade=1&id=4820&page=1

<img width="427" alt="Screen Shot 2021-07-25 at 18 01 16" src="https://user-images.githubusercontent.com/48151790/126896757-102e15ca-6013-42b1-995b-8459595e908f.png">

* Authenticate?

Try: /index.php, /flag., /fl4g.php, ...

- `/index.phps`

<img width="516" alt="Screen Shot 2021-07-25 at 18 05 00" src="https://user-images.githubusercontent.com/48151790/126896839-cf8fdfef-0891-4828-b6cb-a2764a37e9ee.png">

=> Payload = `urlencode(urlencode('admin'));`

![IMAGE 2021-07-25 18:33:27](https://user-images.githubusercontent.com/48151790/126897581-65f7e309-db9e-4a6b-ba74-83c00c8902d5.jpg)

=> Flag

<img width="703" alt="Screen Shot 2021-07-25 at 18 34 16" src="https://user-images.githubusercontent.com/48151790/126897604-ab1a543e-ef44-4e42-8936-b75b91a88a28.png">
