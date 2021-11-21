# README

## users テーブル
| Column                    | Type   | Option                    |
| ------------------------- | ------ | ------------------------- |
| nickname                  | string | null: false               |
| email                     | string | null: false, unique: true |
| encrypted_password        | string | null: false               |

### Association
- has_many :studies


## items テーブル
| Column           | Type       | Option                         |
| ---------------- | ---------- | ------------------------------ |
| study_time       | time       | null: false                    |
| study_language   | enum       | null: false                    |
| other            | string     |                                |
| good_point       | text       | null: false                    |
| notgood_point    | text       |                                |
| thoughts         | text       |                                |
| user             | references | null: false, foreign_key: true |

### Association
- belongs_to :user