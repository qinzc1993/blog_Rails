# blog_ChatGo
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
  - UserRoom

User

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | userName    |  varchar| 24   | user_name   |                                 |
| 3    | password    |  varchar| 60   | password    |                                 |
| 4    | sex         |  varchar| 2    | sex         |                                 |
| 5    | introduction|  varchar| 512  | introduction|                                 |
| 6    | authorityId  |  int| 4   | authority_id|                                 |

```sql
CREATE TABLE `users` (
  `user_id` varchar(24) NOT NULL DEFAULT '',
  `user_name` varchar(24) NOT NULL,
  `password` varchar(60) NOT NULL,
  `sex` varchar(2) DEFAULT NULL,
  `introduction` varchar(512) DEFAULT NULL,
  `authority_id` int(4) NOT NULL,
  `create_time` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (`user_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

Authority

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------:   |
| 1    | authorityId      |  int | 2   | authority_id     | primary key               |
| 2    | authorityName    |  varchar| 24   | authority_name   |                            |

```sql
CREATE TABLE `authorities` (
  `authority_id` int(2) NOT NULL DEFAULT '0',
  `authority_name` varchar(24) NOT NULL,
  PRIMARY KEY (`authority_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

Room

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | roomId      |  varchar| 24   | room_id     | primary key                     |
| 2    | roomName    |  varchar| 24   | room_name   |                                 |
| 3    | createrId      |  varchar| 24   | creater_id     | primary key                     |

```sql
CREATE TABLE `rooms` (
  `room_id` varchar(24) NOT NULL DEFAULT '',
  `room_name` varchar(24) NOT NULL,
  `creater_id` varchar(24) NOT NULL,
  `create_time` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (`room_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

ChatMsg

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | roomId    |  varchar| 24   | room_id   | primary key                         |
| 3    | messageId    |  varchar| 24   | message_id    | primary key                  |
| 4    | message    |  varchar| 1024   | message    |                                 |
| 5    | sendTime    |  timestamp| 24   | create_time    |                              |

```sql
CREATE TABLE `chat_msgs` (
  `user_id` varchar(24) NOT NULL,
  `room_id` varchar(24) NOT NULL,
  `message_id` varchar(24) NOT NULL,
  `message` varchar(1024) DEFAULT NULL,
  `create_time` timestamp NOT NULL DEFAULT '0000-00-00 00:00:00' ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (`user_id`,`room_id`,`message_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

UserRoom

| No  | name |  type |  length  | tableRowName  | introduction  |
| :--  | :--------- |  ----:  | :--  | :--------  | :-----------------------------:   |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | roomId      |  varchar| 24   | room_id     | primary key                     |

```sql
CREATE TABLE `user_rooms` (
  `user_id` varchar(24) NOT NULL,
  `room_id` varchar(24) NOT NULL,
  `create_time` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (`user_id`,`room_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```
