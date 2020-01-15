# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:


## usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, |
|user_name|string|null: false, unique: true|
|e-mail|string|null: false, unique: true|
|password|string|null: false, unique: true|

### Association
- has_many : groups, through: : groups_users
- belongs_to :user
- belongs_to :user
- belongs_to :user


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|group_name|string|null: false |

### Association
- has_many : users, through: : groups_users
- belongs_to : group


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|body|text| null:false |
|image|string|  |

### Association
- belongs_to : message 
- belongs_to : message 
- belongs_to : message 
- belongs_to : message 


## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user



* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
