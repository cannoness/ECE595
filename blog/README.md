# README

## Commands used for first iteration
```
$ rails new blog
hellow
$ cd blog/
$ rails generate scaffold Post title:string body:text
$ rails generate scaffold Comment post:references body:text
$ rake db:migrate
```
## Commands used for second iteration
In this iteration we create users with roles using `rollify`. We define
following roles
1. user
  * Can view posts.
  * Can comment on posts.
2. guest
  * Can view posts.
3. follower
  * Can view posts
  * Can comment on posts.
  * Will be notified if the post is edited or a new comment is posted.
4. moderator
  * Can view posts.
  * Can delete posts.
  * Can comment on posts.
5. author
  * Can create post.
  * Can comment on posts.
  * Can edit his own posts.
### Instructions and commands
#### Generating users scaffold
```
$ rails generate scaffold user email:string
$ rake db:migrate
```
#### Installing rolify
Add following line to `Gemfile` under application root.
```
gem 'rolify'
```
Execute `bundle install` to install required gems.
