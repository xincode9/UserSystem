UserSystem
==========
Ruby On rails 

1.建立Project 注意- 該建立Project的資料庫是mysql

rails new usersys -d=mysql

-d：是在建立建立Project的時候指定所用的資料庫

2.建立一個首頁(新增加一個controller)進入usersys項目
rails generate controller home index

3.希望 index.html.erb作為首頁
修改 routes.rb
 root :to => 'home#index'
 
4.database.yml （修改資料庫的配置文件）

5.打開網頁 powder open


6.建立用戶管理系統表(注意 在資料庫中建立表時 要把表名創建為複數)

 create table users
(
  id int primary key auto_increment,
 name varchar(30),
 password varchar(30)
);

7.使用scaffold產生users表對應的頁面支架

rails generate scaffold user id:int name:varchar password:varchar
