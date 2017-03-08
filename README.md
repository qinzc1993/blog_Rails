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


| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :---------: |  ----:  | :--  | :--------:  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | userName    |  varchar| 24   | user_name   |                                 |
| 3    | password    |  varchar| 60   | password    |                                 |
| 4    | sex         |  varchar| 2    | sex         |                                 |
| 5    | userAuthorityId|  varchar| 24   | user_authority_id   |                                 |
| 6    | introduction|  varchar| 512  | introduction|                                 |

ChatMsg

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :---------: |  ----:  | :--  | :--------:  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | roomId    |  varchar| 24   | room_id   | primary key                         |
| 3    | messageId    |  varchar| 24   | message_id    | primary key                  |
| 4    | message    |  varchar| 1024   | message    |                                 |
| 5    | sendTime    |  timestamp| 24   | send_time    |                              |

Room

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :---------: |  ----:  | :--  | :--------:  | :-----------------------------: |
| 1    | roomId      |  varchar| 24   | room_id     | primary key                     |
| 2    | roomName    |  varchar| 24   | room_name   |                                 |


