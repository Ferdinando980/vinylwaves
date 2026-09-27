<p align="center"><img src="vnl/src/main/webapp/assets/images/Logo.png" width="88" alt="VinylWaves logo"></p>

<h1 align="center">VinylWaves</h1>

<p align="center">A Java web shop for vinyl records, CDs and turntables, developed as a university Web Technologies project.</p>

<p align="center"><b>English</b> · <a href="README.it.md">Italiano</a></p>

![VinylWaves home page](docs/images/vinylwaves-home.png)

## About the project

VinylWaves was built by a three-person university team to take an e-commerce application through the full server-rendered Java stack: catalogue browsing, search and filters, accounts, cart, checkout, order history and back-office catalogue/order management.

This repository is kept public as a record of that coursework. It shows what we built at that point in our studies; it is not presented as a current production shop or as a solo project.

## Main flows

- browse and filter vinyl, CD and turntable products;
- inspect product details and search the catalogue;
- create an account, sign in and edit the profile;
- manage a session-backed cart and complete an order;
- review previous orders;
- manage products and order status through role-specific server routes;
- validate forms in the browser and again on the server.

## Architecture

The application follows a classic MVC-style Java web structure. Jakarta Servlets receive requests, JSP pages render the response, JavaBeans carry domain data and DAO classes isolate SQL access to MySQL.

![VinylWaves architecture](docs/images/vinylwaves-architecture.svg)

The repository includes the database schema in `vnl_db.sql`. Database credentials and the concrete `DBManager.java` are intentionally not versioned.

## Run locally

The original project targets Java 21, Maven, Jakarta Servlet 5 and MySQL. Import `vnl_db.sql`, provide the local database connection expected by the DAO layer, then package the web application:

```sh
cd vnl
./mvnw package
```

Deploy the generated WAR to a compatible Jakarta Servlet container such as Tomcat 10. The checked-in `target/` directory is a historical course artifact; a clean build should be preferred when the private database configuration is available.

## Stack

Java 21 · Jakarta Servlet/JSP · Maven · MySQL · JDBC/DAO · HTML · CSS · JavaScript · JSON/XML

## Team

- Ferdinando Gregorio Fernandez ([@Ferdinando980](https://github.com/Ferdinando980))
- Antonio Ceruso ([@Ceuto](https://github.com/Ceuto))
- Giulia Ferraro ([@g.ferraro34](https://github.com/g.ferraro34))

## Academic context

Developed for the *Tecnologie Software per il Web* course. The README documents the system and each contributor is credited; the code remains a snapshot of the university project rather than a rewritten portfolio demo.

## License

Copyright © 2025 the VinylWaves contributors. All rights reserved. The source is visible for academic and portfolio evaluation; reuse, redistribution and derivative works are not permitted. See [LICENSE](LICENSE).
