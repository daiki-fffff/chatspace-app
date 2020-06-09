## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|username|string|null: false|
|password|string|null: false|

### Association
- has_many :messages
- has_many :posts

## messageテーブル
|Column|Type|Options|
|-------|----|-------|
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :post
- belongs_to :user

## Group_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

# postsテーブル
|Column|Type|Options|
|-------|----|-------|
|text|text|null: false|
|image|string|

### Association
- has_many :messages
- has_many :users