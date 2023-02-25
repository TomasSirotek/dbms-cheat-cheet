****

#### Description

* **high-level** modules should **not** depend on low-level modules, but both should depend on **abstractions**. Abstractions should **not** depend on details; details should **depend** on abstractions.

* In other words, instead of writing code that depends on **concrete** implementations, we should write code that depends on **interfaces** or **abstract** classes. This makes our code more **flexible**, **maintainable**, and easier to **test**.

*Example of violations of the Open-closed principles 

```java

public class ReportingService {
    private EmailSender emailSender; // low-level-module

    public ReportingService() {
        this.emailSender = new EmailSender();
    }

    public void generateReport() {
        // generate report

        // send email notification
        emailSender.sendEmail("Report generated");
    }
}

```

* In this example `ReportingService` depends on the `EmailSender` **low-level module**. 
* In this case if we want to change the way we send email notif, we would need to modify the `ReportingService` that is not **incorrect**

*Correct approach of using interface/abstraction 

```java 

public interface EmailService {
    void sendEmail(String message);
}

public class EmailSender implements EmailService {
    @Override
    public void sendEmail(String message) {
        // send email
    }
}

public class ReportingService {
    private EmailService emailService;

    public ReportingService(EmailService emailService) {
        this.emailService = emailService;
    }

    public void generateReport() {
        // generate report

        // send email notification
        emailService.sendEmail("Report generated");
    }
}

```