# CS-305-Software-Security
Artemis Financial Practices for Secure Software Report
Artemis Financial is a consulting company that develops individualized financial plans for its customers, including savings, retirement, investments, and insurance. To modernize its operations, Artemis Financial’s goal was to add a file verification step to its web application and ensure secure communications.

To meet these goals, I implemented a keystore and generated a self-signed certificate. This certificate was used while generating a checksum to confirm the integrity of files and to support secure connections. In addition, I configured the application to automatically route all HTTP traffic to secure HTTPS, ensuring that all communication between clients and the server is encrypted. These measures help protect sensitive customer information and build user trust by providing secure end-to-end encrypted (E2EE) communications.

After verifying that the hash algorithm generated a proper checksum and that the application successfully established HTTPS connections, I ran a dependency check to confirm that no new vulnerabilities were introduced into the system.

Challenges Encountered

The most difficult part of the vulnerability assessment process was identifying false positives in the dependency check results. Distinguishing between actual security threats and non-critical findings required careful review.

The longest portion of the project was configuring the environment to generate a checksum. Initially, I struggled with getting the command prompt to recognize the keytool. After learning how to properly set the system path to the Java JDK and keytool utility, I was able to successfully generate certificates and checksums. From that point on, the remaining implementation went smoothly.

Final Outcome

After refactoring the code, I uploaded the .cer file containing the self-signed certificate I created. I then confirmed that the application successfully established a secure HTTPS connection and generated the correct checksum for file verification.

Through these steps, I was able to strengthen Artemis Financial’s application by:

    ~Implementing secure HTTPS communication.

    ~Generating and validating a checksum for file verification.

    ~Using a self-signed certificate stored in a keystore.

    ~Running dependency checks to ensure no vulnerabilities were introduced.

These practices align with industry-standard secure coding guidelines and provide Artemis Financial with an enhanced security posture for protecting sensitive customer financial data.

To a future employer I would point out that this assignment demonstrates skills such as:
    
    Secure coding best practices (OWASP) 
    
    SSL/TLS certificate generation and management
    
    Checksum and hash verification
    
    Vulnerability assessment
    
    Problem solving under real world constraints
