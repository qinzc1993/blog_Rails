# blog_Rails
study Rails.
***
## project name: ChatGo
  author: Rasin qzc.
### project introduction：
  chat rooms online;
  
### database: MySql;
  - User  
  - Authority
  - Room
  - ChatMsg

User

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | userName    |  varchar| 24   | user_name   |                                 |
| 3    | password    |  varchar| 60   | password    |                                 |
| 4    | sex         |  varchar| 2    | sex         |                                 |
| 5    | introduction|  varchar| 512  | introduction|                                 |

Authority

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | authorityId      |  varchar| 4   | authority_id     | primary key                     |
| 2    | authorityName    |  varchar| 24   | user_name   |                                 |

Room

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | roomId      |  varchar| 24   | room_id     | primary key                     |
| 2    | roomName    |  varchar| 24   | room_name   |                                 |

ChatMsg

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | roomId    |  varchar| 24   | room_id   | primary key                         |
| 3    | messageId    |  varchar| 24   | message_id    | primary key                  |
| 4    | message    |  varchar| 1024   | message    |                                 |
| 5    | sendTime    |  timestamp| 24   | send_time    |                              |

