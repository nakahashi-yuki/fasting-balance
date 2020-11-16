# テーブル設計

## users テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| nickname           | string  | null: false |
| email              | string  | null: false |
| encrypted_password | string  | null: false |
| height             | integer | null: false |
| target_body_weight | integer | null: false |
| motion_id          | integer | null: false |
| week_motion_id     | integer |             |

### Association
- has_many :personals
- has_many :memos

## personals テーブル

| Column      | Type    | Options     |
| ----------- | ------- | ----------- |
| body_weight | integer | null: false |

### Association
- has_many :memos
- belongs_to :user

## memos テーブル

* How to run the test suite
| Column   | Type    | Options     |
| -------- | ------- | ----------- |
| title_id | integer | null: false |
| memo     | text    | null: false |

### Association
- belongs_to :personal
- belongs_to :user
