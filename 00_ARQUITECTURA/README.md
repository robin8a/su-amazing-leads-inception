# Opciones

## Serverless 
### Base de datos
- No relacional (DynamoDB) con el fin de poder agregar campos dinámicos. Los contemplamos en éste momento?
- Al ser preguntas (dicotómicas) la estructura sería (ID, PREGUNTA, VALOR)
- Pros: Serverless solo se paga por el uso de escritura/lectura, el API queda disponible para futuras versiones moviles (ex. react-native)
- Cons: Para los reportes de agregación complejos com (AVG, SUM, COUNT, etc), cambios en BD de indices a veces es neceario borrar la BD

### Lógica del negocio
- AppSync/GraphQL
- Pros: código autogenerado por AppSync, se paga solo por el uso

# UI/Ux
- react-js

## API (microsevicios)

### Base de datos
- Relacional (ex. Postgress), usar el tipo de dato JSON para el uso de campos dinámicos

### Lógica del negocio
- RESTful API
- La logica se hace en funciones LAMBDA
- Pros: total control de API
- Cons: mayor tiempo de desarrollo debido a que no hay 

# UI/Ux
- react-js


# Autorización y Autenticación
- AWS Cognito

# Despliegue
- Por cada proyecto generar su propia estructura (ui/appsync/db)
- Una sola aplicación donde distiguimos a traves de "proyectos el contenido a desplegar", aquí lo dificil es mantener separado los URLs y marcas. Quiero decir, por ejemplo encuesta.bancosantander.com de encuesta.otra_empresa.com ya que se tiene la misma raíz.

# Testing Web-App

- [Amplify master branch](https://master.ds3q4dungfi7s.amplifyapp.com/)

# API Appsync

## Postman
- Use postman
- 

## AWS - cli scan command
