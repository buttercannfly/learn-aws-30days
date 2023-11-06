# Term

## What does IAM do?

who access what

## User vs Role

| User                          | Role             |
| ----------------------------- | ---------------- |
| long-term access              | temporary access |
| ｜ associated with one person | customized       |

IAM Role

1. 联合用户访问
2. 临时 IAM 用户权限
3. 跨账号权限
4. 跨服务权限

Policy

某用户可以对某资源有某种权限

When to use AWS user ?

1. 第三方 aws 客户端
2. 不支持 role 的 aws 资源，如 Wordpress 插件
3. AWS CodeCommit
4. 紧急情况

When to use IAM role ?

1. AWS EC2
2. Mobile App
3. 对员工的一次身份验证，而不是登入 AWS 控制台

What's Policy

````
{
  "Version": "2012-10-17",
  "Statement": {
    "Effect": "Allow",
    "Action": "dynamodb:*",
    "Resource": "arn:aws:dynamodb:us-east-2:123456789012:table/Books"
  }
}```

allow to any dynamodb actions on Resource: arn:aws:dynamodb:us-east-2:123456789012:table/Books
````
