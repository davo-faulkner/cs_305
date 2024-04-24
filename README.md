# cs_305

This fictional client, Artemis Financial, is a consulting company that develops individualized financial plans for their customers. The financial plans include savings, retirement, investments, and insurance. The client wanted to modernize their operations and use the most current and effective software security.

Specifically, Artemis Financial wanted to add a file verification step to their web application to ensure secure communications. When the web application is used to transfer data, they needed a data verification step in the form of a checksum.

They also wanted a SSL certificate to be generated so that communication could be secured on their web application.

I chose the SHA-256 cipher algorithm for the checksum since it has no known collisions to date, has never been broken, and is recommended by NIST for hashing. I also generated a self-signed certificate for the client to secure communications.

It's important to code securely to avoid data breaches of clients and customers in addition to avoiding fines when working with sensitive health and financial data.

Early in the term, the static testing was challenging since the NVD was down for a few days, and I wasn't sure if the error was mine or NIST's; however, that was resolved fairly quickly. Later on, integrating the self-signed certificate into the RESTful API was a bit difficult, but I eventually figured it out after some additional research.

Layers of security were increased through this and earlier projects through the use of static dependency checking using OWASP's Dependency-Check Maven plug-in (including the suppression of false positives), using SHA-256 hashing to generate checksums for data validation, manual code review, and SSL certificate generation and integration.

At a high level, I would use the Vulnerability Assessment Process Flow Diagram, my textbook resources, and the linked resources from the class (which I saved) to assess vulnerabilities and determine which mitigation techniques to use.

I made certain the code and software application were functional and secure by checking for errors during the build and run processes. I made sure that no additional vulnerabilities were introduced through my refactoring by documenting the total number of vulnerable dependencies before and after refactoring. Note that this project did not require mitigating all vulnerable dependencies. That process was learned in previous lessons and projects.

Tools that will be useful in later projects are the Java keytool.exe application, OWASP's Dependency-Check Maven plug-in, the NIST NVD, and the Eclipse Keytool plug-in.

The entire code base from this assignment is also available for review for which I received a grade of 100%.
