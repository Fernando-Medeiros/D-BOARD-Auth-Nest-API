# DashBoard - Auth - NestJS - API

![Node](https://img.shields.io/badge/Node.JS-white?style=for-the-badge&logo=node.js&logoColor=black)
![Nest](https://img.shields.io/badge/Nest.JS-white?style=for-the-badge&logo=nestjs&logoColor=black)
![Jest](https://img.shields.io/badge/Jest-white?style=for-the-badge&logo=jest&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-white?style=for-the-badge&logo=TypeScript&logoColor=black)
![Prisma](https://img.shields.io/badge/Prisma-white?style=for-the-badge&logo=prisma&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-white?style=for-the-badge&logo=Docker&logoColor=black)
![Postgres](https://img.shields.io/badge/Postgres-white?style=for-the-badge&logo=postgresql&logoColor=black)
![Swagger](https://img.shields.io/badge/Swagger-white?style=for-the-badge&logo=swagger&logoColor=black)

## Usage

- [START](START.md)
- [PRISMA CLI](PRISMA.md)

## Dependencies

- This project relies on an email with remote access permission

## Routes

### **/login**

> @POST |
>
> @BODY
>
> - email
> - password

### **/refresh**

> @POST | @PARAM(**:token**)

### **/customer**

#### _Register Customer_

> @POST
>
> @BODY:
>
> - firstName
> - lastName
> - email
> - password

#### _Find Many Customers  -> **/customer/find**_

> @SESSION | @GET
>
> @QUERY:
>
> - limit = 10 || ???
> - order = asc || desc
> - sort = columns -> id | email | firstName | lastName | createdAt

#### _Get Own Customer_

> @SESSION | @GET

#### _Delete Customer_

> @SESSION | @DELETE

#### _Update Customer_

> @SESSION | @PATCH
>
> @BODY:
>
> - firstName
> - lastName
> - email

### **/password**

#### _Recover Password_

> @POST
>
> @BODY:
>
> - Email

#### _Reset Password_

> @PUT | @PARAM(**:token**)
>
> @BODY:
>
> - password

#### _Update Password_

> @SESSION | @PATCH
>
> @BODY:
>
> - password.

## Preview

![preview](d-board-preview.png)
