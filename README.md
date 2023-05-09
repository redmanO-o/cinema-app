# 🎦 Cinema-app
This application demonstrates how a cinema ticket reservation system works. 
Built in accordance with the concepts of N-tier architecture,
REST principles and using Spring and Hibernate frameworks.
In addition to management functions, user authentication mechanisms 
and division into user and admin roles are also implemented.

######  🔗 _project navigation_
- [Project description](#-cinema-app)
- [Features](#-features)
- [How to run](#-how-to-run)
- [Project structure](#-project-structure)
- [Used technologies](#-used-technologies)
- [Link](#-author)


### 💫 Features

- Role-based access control

`USER` role:
1. Find movies and cinema halls
1. Find available movie sessions
1. Create shopping cart
1. Add tickets to shopping cart
1. View shopping cart
1. Make an order
1. View order history

`ADMIN` role:
1. Management: `cinema halls`, `movies` and `movie sessions`
2. Access to users information

### ▶️ How to run
- ✅ [Clone](https://github.com/redmanO-o/cinema-app/fork) the project from GitHub
- ✅ Configure [db.properties](src/main/resources/db.properties)
   with your own URL, username, password and JDBC driver 
- ✅ Configure Tomcat server (it is recommended to use version
   [9.0.73](https://tomcat.apache.org/download-90.cgi#9.0.73) ❗️)
- ✅ Use Postman for communication with app
  - `POST /register` - register new user (non-auth access);
  - `GET /movie-sessions/available` - get list of sessions (user, admin);
  - `GET /cinema-halls` - get list of halls (user, admin);
  - `GET /users/by-email` - retrieve user's info (admin);
  - `POST: /cinema-halls ,/movies, /movie-sessions` - create corresponding objects (admin);
  - `PUT, DELETE /movie-sessions` - update and delete movie session (admin);
  - `GET /orders /shopping-carts/by-user` - show history of orders, list of tickets in cart (user);
  - `PUT /shopping-carts/movie-sessions` - put a ticket on this movie session to the cart (user);
  - `POST /orders/complete` - execute order (user);
- ✅ Default credentials for access
  -  login: `admin@i.ua`, password: `admin123` (admin)
  -  login: `user@i.ua`, password: `user1234` (user)
     
🚀 Login and enjoy the program

### 📂 Project structure
+ [**Config**](src/main/java/cinema/config)
  _(framework's configuration)_
+ [**Controller**](src/main/java/cinema/controller) 
_(client-server communication)_
+ [**DAO**](src/main/java/cinema/dao) 
_(access to DB)_
+ [**DTO**](src/main/java/cinema/dto) 
_(objects for models custom representation)_
+ [**Exception**](src/main/java/cinema/exception) 
_(custom exception)_
+ [**Lib**](src/main/java/cinema/lib) 
_(custom annotations & validation methods)_
+ [**Model**](src/main/java/cinema/model) 
_(objects/entities used in the application)_
+ [**Security**]() 
_(determination of user's access level)_
+ [**Service**](src/main/java/cinema/service) 
_(business logic)_
  + [**Mapper**](src/main/java/cinema/service/mapper) 
  _(dto-model / model-dto transformation)_ 
+ [**Util**](src/main/java/cinema/util) 
_(DateTime pattern)_

### ⚙️ Used technologies

| Technology          |   Version    |
|---------------------|:------------:|
| JDK                 |      17      |
| Maven               |    3.1.1     |
| Spring              |    5.3.20    |
| Spring Security     |    5.6.10    |
| Hibernate           | 5.6.14.Final |
| Hibernate validator | 6.1.6.Final  |
| TomCat              |    9.0.73    |
| MySQL               |    8.0.22    |
| Javax annotation    |    1.3.2     |
| Javax servlet       |    4.0.1     |
| Jackson core        |    2.14.1    |


### 📌 Author
#### Oleksandr Krasnov <br/>[LinkedIn](https://www.linkedin.com/in/oleksandr-krasnov-106415234)