## Sharing

This application consists of Projects that belong to Users.

After completing the exercises, Users should be able to share their Projects with other Users.
Users should be able to follow other users as well.

## Exercise 1 - Model testing

### Project Sharing

Add a method to Project class called share_with, with the following signature.

```
project.share_with(users)
```

Add a method for users to get the shared projects, and all visible projects.

```
user.projects
user.shared_projects
user.visible_projects (user.projects + user.shared_projects)
```

Implement model tests to ensure all these new methods are still working.


### User Following

Add a method to User called follow, with the following signature:

```
user.follow(other_user)
```

Add the following methods to user as well:

```
user.followers (the users that are following user)

user.following (the users that user is following)
```

Implement the model tests to ensure these methods are working.


## Exercise 2 - Controller test
Implement a controller with a share action in the projects controller. Implement its corresponding controller test.


## Exercise 3 - Feature test
Implement a feature test that:

* logs in user (user1)
* visit the project detail view
* select a popup of users and select another user (user2) to share the project with
* click submit to share the project with that user
* log out user1
* log in as user2
* visit the projects index page
* test that user2 can view the project just shared in the user2 project listing view (you will need to modify the index action to include all visible projects for user2)

## Test Coverage
Testing is at 100%. As you add these features, keep the testing at 100%

## Testing Gems
This application uses Fabrication for fabricators, rspec for testing. For the integration test, you can optionally
use cucumber instead of rspec features.

## Front End
Run the rake db:seed to seed the database with users and projects.
Users are user_1@sharing.com, password: "password" for all of them.
Users go from user_1 to user_10.

### Ruby, Rails
This application is using Ruby 2.1.1 and Rails 4.1.1.

### To get started
```
$ bundle
$ rake db:create
$ rake db:migrate
$ rspec
```





