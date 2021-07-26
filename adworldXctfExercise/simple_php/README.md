# Challenge: https://adworld.xctf.org.cn/task/answer?type=web&number=3&grade=0&id=5072&page=1

<img width="430" alt="Screen Shot 2021-07-26 at 17 46 42" src="https://user-images.githubusercontent.com/48151790/126977068-056f3bfc-687d-481a-8652-a846166278a8.png">

  `$a == 0 and $a` => payload: `?a=0x`
  
  `if(is_numeric($b)) exit();` => b is not a number.
  
  `$b>1234` => payload: `?b=1235x`

<img width="542" alt="Screen Shot 2021-07-26 at 17 47 18" src="https://user-images.githubusercontent.com/48151790/126977158-6b6b0bab-dd54-4cea-b04c-a7b43902c8d9.png">
