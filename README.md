# テーブル設計

## users テーブル

| Column             | Type    | Options     |
| ------------------ | ------  | ----------- |
| email              | string  | null: false |
| encrypted_password | string  | null: false |
| shop_name          | string  | null: false |
| person_name        | string  | null: false |
| postal_code        | integer | null: false |
| address            | string  | null: false |

### Association

- has_many :cars

## cars テーブル

| Column       | Type       | Options                        |
| ------------ | ---------- | ------------------------------ |
| price        | integer    |                                |
| car_maker    | string     | null: false                    |
| car_model    | string     | null: false                    |
| car_grade    | string     |                                |
| body_color   | string     |                                |
| vi_number    | string     | null: false                    |
| year         | integer    | null: false                    |
| mileage      | integer    | null: false                    |
| drive_system | string     | null: false                    |
| transmission | string     | null: false                    |
| inspection   | integer    |                                |
| user         | references | null: false, foreign_key: true |

### Association

- belongs_to :user
