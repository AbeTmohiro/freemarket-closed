# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation
# DATABASE
## addressテーブル
|Column|Type|Options|
|------|----|-------|
|phone_number|string|
|postal_code|string|
|prefecture|integer|default: 0|
|city|string|
|house_number|string|
|building_name|string|Key: pri|
|user_id|bigint(20)|key: mul|

### Association
- has many :messages
- has_many :groups_users
- has_many :groups,through: :groups_users

## brand_groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|

### Association
- has_many :groups_users
- has_many :users,through: :groups_users
- has_many :messages

## brand_namesテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false,unique: true|

### Association
- belongs_to :group
- belongs_to :user

## brandname_brandgroupsテーブル
|Column|Type|Options|
|------|----|-------|
|brand_name_id|bigint(20)|null: false,key: mul|
|brand_group_id|bigint(20)|null: false,key: mul|

### Association
- belongs_to :group
- belongs_to :user

## cardsテーブル
|Column|Type|Options|
|------|----|-------|
|customer_token|string|null: false|
|user_id|bigint(20)|null: false, key: mul|

### Association
- belongs_to :user

## categoriesテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|ancestry|string|

### Association
- belongs_to :group
- belongs_to :user

## category_brandgroupsテーブル
|Column|Type|Options|
|------|----|-------|
|category_id|bigint(20)|null: false,key: mul|
|brand_group_id|bigint(20)|null: false,key: mul|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## category_sizegroupsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## comment_itemsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## dealing_chat_messagesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## dealingsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## item_brandsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## item_imagesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## item_sizesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## itemsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## likesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## size_groupsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## sizesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## sns_credentialsテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## valuesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text|
|image|string|
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
