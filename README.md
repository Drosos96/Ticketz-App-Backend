Ticketz Application

Περιγραφή

Η Ticketz είναι μία εφαρμογή για τη διαχείριση εισιτηρίων για διάφορα events, όπως θέατρα, σινεμά, αθλητικά γεγονότα και μουσικές συναυλίες. 
Η εφαρμογή επιτρέπει τη δημιουργία, επεξεργασία και διαγραφή χρηστών, events και εισιτηρίων.

Δημιουργία Build

Απαιτήσεις:

Χρειάζεται Java 17.
Χρειάζεται Maven.
Δημιουργήθηκε με MySQL και απαιτεί μία βάση δεδομένων.


Εκτελέστε την παρακάτω εντολή για να δημιουργήσετε μία νέα βάση δεδομένων:

CREATE DATABASE ticket_system;


Ρύθμιση του αρχείου application.properties:

Εντοπίστε το αρχείο application.properties στον φάκελο src/main/resources.

spring.datasource.url=jdbc:mysql://localhost:3306/ticket_system?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=UTC
spring.datasource.username=drosos
spring.datasource.password=12345
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.format-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect


Δημιουργία του Build:

Μεταβείτε στον φάκελο του project.
Εκτελέστε την εντολή:

mvn clean install

Το αρχείο ticketz-0.0.1-SNAPSHOT.jar θα δημιουργηθεί στον φάκελο target/.


Deploy της Εφαρμογής

Εκκίνηση της Εφαρμογής:

java -jar target/ticketz-0.0.1-SNAPSHOT.jar

Η εφαρμογή θα είναι διαθέσιμη στη διεύθυνση: http://localhost:8080
