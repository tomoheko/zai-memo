# README
## usersテーブル
| Column            | Type       | Options     |
| ----------------- | ---------- | ----------- |
| name              | string     | null: false |
| email             | string     | null: false |
| password          | string     | null: false |

### Association
- has_many :lists



## listsテーブル
| Column           | Type       | Options                        |
| ---------------- | ---------- | ------------------------------ |
| title            | string     | null: false                    |
| user             | references | null: false, foreign_key: true |

### Association
- belongs_to :user
- has_many   :tags



## tagsテーブル
| Column  | Type       | Options                        |
| ------- | ---------- | ------------------------------ |
| name    | text       | null: false                    |
| price   | integer    | null: false                    |
| list    | references | null: false, foreign_key: true |

### Association
- belongs_to :list