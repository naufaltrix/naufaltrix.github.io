---
layout: post
title: SqlCoding Shit Post
tags: [sql, shitpost]
comment: true
---

Sql query coding shit post for users & sales

```sql
SELECT users.username,users.email,user_profiles.userId as userId_sales,
user_profiles.name as user_name,user_profiles.phone,
agent_profiles.companyName,brands.name as name_brand from users
LEFT JOIN user_profiles ON user_profiles.userId = users.id
LEFT JOIN brands ON brands.id = user_profiles.userId
LEFT JOIN agent_profiles ON agent_profiles.userId = user_profiles.userId
WHERE users.banned = 0 AND users.activated = 1 
AND user_profiles.referenceId = 36003607412310586
ORDER BY users.id DESC LIMIT 10
```

