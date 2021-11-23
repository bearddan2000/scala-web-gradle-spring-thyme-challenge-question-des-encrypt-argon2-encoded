# scala-web-gradle-spring-thyme-challenge-question-des-encrypt-argon2-encoded

## Description
A springboot challenge-question web app with thymeleaf support.
Three roles are defined; USER, ADMIN, and SUPER. All roles
can access pages `/home`, `/login`, and `/about`. Only USER
can access `/user` and ADMIN only `/admin` whereas SUPER can
navigate to either and have its own `/super`. Each role
has an action USER=VIEW ONLY, ADMIN=READ/WRITE, SUPER=CREATE.
All password are encrypted with DES and encoded with argon2
to insure strong passwords.

Presents a register form to create an inMemoryUser.
Once the user is created it is given the USER role
by default and auto logged in.

Presents a challenge-question form to challenge-question passwords on any user,
by default the user is reassigned USER role and auto
logged in. Only restriction on passwords are they match;
all validation is done client side.

Uses a challenge question on password rest and user register
to verify user. Customizes user data class by extending the
UserDetailService.

## Tech stack
- scala
- gradle
  - springboot
  - thymeleaf
  - bootstrap
  - jquery
  - datatable

## Docker stack
- gradle:jdk11

## To run
`sudo ./install.sh -u`
Available at http://localhost
- Login with id: user and password: pass
- Login with id: admin and password: pass
- Login with id: super and password: pass

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
