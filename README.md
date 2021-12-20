# README

##　users　テーブル

| Column             | Type      |  Option                   |
|--------------------|-----------|---------------------------|
| email              | string    | null: false, unique: true |
| encrypted_password | string    | null: false               |
| name               | string    | null: false               |
| profile            | text      | null: false               |
| occupation         | text      | null: false               |
| position           | text      | null: false               |

### Association

- has_many :comments
- has_many :prototypes


## comments テーブル

| Column    | Type       | Option                        |
|-----------|------------|-------------------------------|
| content   | text       | null: false                   |
| prototype | references | null:false, foreign_key: true |
| user      | references | null:false, foreign_key: true |

### Associarion

- belongs_to :user
- belongs_to :prototype
