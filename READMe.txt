https://www.roytuts.com/python-rest-api-crud-example-using-flask-and-mysql/

Install Python

Install Flask - pip install flask
Install FlaskMySQL - pip install flask-mysql
Install PyMySQL - pip install pymysql
Install werkzeug for password hashing - pip install werkzeug
Install Flask-CORS - pip install flask-cors     //Without this will give error Access to XMLHttpRequest at 'http://localhost:5000/users' from origin 'http://localhost:4200' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource.

create table in database
      CREATE TABLE `tbl_user` (
        `user_id` bigint(20) NOT NULL AUTO_INCREMENT,
        `user_name` varchar(45) COLLATE utf8_unicode_ci DEFAULT NULL,
        `user_email` varchar(45) COLLATE utf8_unicode_ci DEFAULT NULL,
        `user_password` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
        PRIMARY KEY (`user_id`)
      ) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;


GET  http://localhost:5000/users
[
    {
        "user_email": "contact@roytuts.com",
        "user_id": 1,
        "user_name": "Soumitra Roy",
        "user_password": "pbkdf2:sha256:50000$zQLJxLem$40a50a43592f9643a335ef53dc1cdfe312292c428dd4f20c36f8627ef40ee43b"
    }
]



POST  http://localhost:5000/add
{
	"name":"Soumitra",
	"email":"contact@roytuts.com",
	"pwd":"pwd"
}


POST  http://localhost:5000/update
{
	"id":2,
	"name":"Soumitra Roy",
	"email":"contact@roytuts.com",
	"pwd":"pwd"
}

GET http://localhost:5000/delete/2

example
