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
| :-  | :---------: |  ----:  | :--  | :-----------:  | :-----------------------------: |
| 1    | userId      |  varchar| 24   | user_id     | primary key                     |
| 2    | userName    |  varchar| 24   | user_name   |                                 |
| 3    | password    |  varchar| 60   | password    |                                 |
| 4    | sex         |  varchar| 4    | sex         |                                 |
| 5    | userAuthorityId|  varchar| 24   | user_authority_id   |                                 |
| 6    | introduction|  varchar| 512  | introduction|                                 |
