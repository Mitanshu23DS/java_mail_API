````markdown
# Java Mailer API

A simple RESTful API built with Spring Boot to demonstrate email sending functionality using JavaMail and Gmail's SMTP server.

---

## Features

* Exposes a single REST endpoint to trigger email sending.
* Uses Spring Boot's `JavaMailSender` for easy mail integration.
* Configurable via `application.properties` for SMTP server details.
* Built with a clean and straightforward Controller-Service architecture.

---

## Technology Stack

* **Java 17**
* **Spring Boot**
* **Spring Web**
* **Java Mail Sender**
* **Maven**

---

## Prerequisites

Before you begin, ensure you have the following installed:
* JDK 17 or newer
* Apache Maven
* A **Gmail Account** with an **App Password** enabled. (Regular passwords will not work).

---

## Configuration

1.  Clone the repository to your local machine:
    ```bash
    git clone [https://github.com/Mitanshu23DS/Java-mailer-API.git](https://github.com/Mitanshu23DS/Java-mailer-API.git)
    cd Java-mailer-API
    ```
2.  Navigate to `src/main/resources/`.
3.  Create a file named `application.properties`.
4.  Add the following configuration to the file.

    ```properties
    # Server Port
    server.port=8080
    
    # Mail Server Properties for Gmail
    spring.mail.host=smtp.gmail.com
    spring.mail.port=587
    spring.mail.username=YOUR_GMAIL@gmail.com
    spring.mail.password=YOUR_GMAIL_APP_PASSWORD
    
    # Enable STARTTLS for secure connection
    spring.mail.properties.mail.smtp.auth=true
    spring.mail.properties.mail.smtp.starttls.enable=true
    ```

    > **⚠️ Security Warning:**
    > Do not commit the `application.properties` file with your real credentials. Ensure it is listed in your `.gitignore` file to prevent exposing your password.

---

## How to Run the Application

You can run the application using Maven from the project's root directory:

```bash
mvn spring-boot:run
````

The application will start on `http://localhost:8080`.

-----

## API Endpoint

Once the application is running, you can trigger an email by sending a request to the following endpoint.

#### Send a Test Email

  * **Method:** `GET`
  * **URL:** `http://localhost:8080/send-test-email`
  * **Success Response:** A string confirming that the email was sent.

You can test this by opening the URL in your web browser or by using a tool like Postman.

-----

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

-----

## Author

  * **Mitanshu Shinde**
  * GitHub: [@Mitanshu23DS](https://www.google.com/search?q=https://github.com/Mitanshu23DS)

<!-- end list -->

```
```
