---
title: Build your blog by using GitHub and Hexo
date: 2019-03-31 23:35:55
tags:
---

## Introduction

I had used Logdown as my Blog before, it's a blog base on Markdown that's why it's popular for engineers. As the author is no longer maintained it, I'm look forward to find a new one to replace it, also based on Markdown. I think GitHub & Hexo is a good solution for me.

My environment is MAC Mojave 10.14.3.
If you are also use MAC but the os version is not same, do not worry too much about it.
 
 
### The following steps are

1. Install Node
2. Install Hexo
3. Create a new GitHub repository
4. Initial your Hexo project
5. Deploy to GitHub
  
## 1. Install Node

You can install it on their official website directly. [Node.js](https://nodejs.org/en/) 
 
or 
 
If you have many projects and some of them are using different Node versions. I recommond you can use [NVM](https://github.com/creationix/nvm).
 
 
## 2. Install Hexo

Install Hexo Git 

`npm install hexo-deployer-git --save` 

Install Hexo 
 
`npm install hexo-cli -g` 
 
Install Hexo deployer git 
 
`npm install hexo-deployer-git --save` 
 
Check Hexo version 
 
`hexo version` 

## 3. Create a new GitHub repository

Repository name : yourname.github.io (change yourname to your GitHub Id)
![](https://i.imgur.com/zPbZWhz.png)

## 4. Initial your Hexo project

Initial blog 

`hexo init blog`

Change directory 

`cd blog`

Install node module 

`npm install`

Host on your local 

`hexo serve`

You will see your Hexo project is running at [http://localhost:4000](http://localhost:4000)

## 5. Deploy to GitHub

Go to the _config.yml and find the deploy area. 
(change yourname to your GitHub Id)

```
deploy:
  type: git
  repository: https://github.com/yourname/yourname.github.io.git
  branch: master
  yourname: yourname
```

Deploy 

`hexo deploy -generate`

Then you can see your blog on the GitHub.

## Conclusion

Hexo is a great tool that you can build your own blog easily in a short time. And there are many powerful plug-ins. I changed the theme that you can find blow the reference or you can choose one you liked [here](https://hexo.io/themes/index.html). It looks better now!


## Reference
1. [Node.js管理神器nvm](https://medium.com/%E5%93%86%E5%95%A6%E5%AF%A6%E9%A9%97%E5%AE%A4/node-js%E7%AE%A1%E7%90%86%E7%A5%9E%E5%99%A8nvm-b6acfca44ea5)
2. [Hexo+GitHub，新手也可以快速建立部落格](https://yaoandy107.github.io/hexo-tutorial/)
3. [hexo d命令报错 ERROR Deployer not found: git](https://blog.csdn.net/qq_21808961/article/details/84476504)
4. [hexo-theme-icarus](https://github.com/ppoffice/hexo-theme-icarus)
