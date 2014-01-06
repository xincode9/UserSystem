UserSystem
==========

1：創建項目 注意- 該項目默認的資料庫是mysql
rails new usersys -d=mysql
-d：是在創建項目的時候指定所用的數據庫
2:創建一個首頁(新增加一個控制器)進入usersys項目
rails generate controller home index
3：修改 F:\bfRails\usersys\app\views\home下面的index.html.erb文件

4:希望 index.html.erb作為首頁
修改F:\bfRails\usersys\config下面 routes.rb
 root :to => 'home#index'
5：database.yml （修改數據庫的配置文件）
6：打開網頁 powder open



7:創建用戶管理系統表(注意 在資料庫中創建表時 要把表名創建為複數)
 create table users
(
  id int primary key auto_increment,
 name varchar(30),
 password varchar(30)
);
9:使用scaffold產生users表對應的頁面支架
rails generate scaffold user id:int name:varchar password:varchar
