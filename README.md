# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:


## usersテーブル
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, |
|user_name|string|null: false, unique: true|
|e-mail|string|null: false, unique: true|
|password|string|null: false, unique: true|


### Association
- has_many : group_id, : : groups_users
- has_one : user_id
- has_one : user_name
- has_one : e-mail
- has_one : password


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|group_name|string|null: false |

### Association
- has_many : user_id, through : groups_users
- has_one : group_id
- has_one : group_name


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|body|text| null:false |
|image|string|  |

### Association
- belongs_to : user_id 
- belongs_to : group_id 
- has_one : body
- has_one : image


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
