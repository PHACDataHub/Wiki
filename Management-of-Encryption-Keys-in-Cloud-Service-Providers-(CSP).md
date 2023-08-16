## **Key Terminology**

To ensure clarity and consistency throughout this documentation, let's define the key terms:

- **CSP (Cloud Service Provider)**: An entity offering cloud-based platforms, infrastructures, applications, or storage services.
- **Key**: Represents an encryption unit. Symmetric keys have the capability to both encrypt and decrypt data. Meanwhile, Asymmetric Keys work in tandem - a public key encrypts data without the ability to decrypt it, and a corresponding private key handles decryption. Additionally, Asymmetric Private keys are instrumental in data signing, validating the authenticity and integrity of data.
- **Multi-Cloud**: A strategy involving the utilization of diverse Cloud Service Providers. For instance, a system integrated with both AWS and Azure epitomizes multi-cloud architecture.
- **Hybrid Cloud**: This pertains to a system that leverages services from both a cloud provider and an on-premises datacenter. A blend of AWS and SSC DataCentres serves as an archetype for a hybrid cloud model.

## **Overview of Key Management Approach**

Within the confines of our organization, we vest confidence in CSPs to oversee and handle the encryption keys diligently. Recognizing the trust we place in CSPs for managing our computational and storage assets, it's a logical extension to trust them with the vital task of encryption on our behalf.

However, operational necessities might occasionally necessitate our intervention in supplying encryption keys. The motives for such interventions could range widely, and to illuminate this further, we've enumerated a few non-exhaustive scenarios:

- Should there be an imperative to encrypt/decrypt beyond the scope of a singular account (spanning across multi-cloud, hybrid cloud, multiple accounts, and so forth).
- In instances where the key rotation duration prescribed by the CSP does not resonate with our security stance.
- Specific situations demanding the use of asymmetric encryption to cater to particular security or functional requirements.

## **Key Management Best Practices**

To uphold our stringent security and compliance mandates, it's quintessential to adopt best practices in key management:

* **Trust But Verify**: While we trust CSPs with key management, periodic audits and reviews of their practices ensure transparency and adherence to our security norms.
* **Documented Exceptions**: Any deviation from the standard procedure, like providing our own keys, must be documented, providing clear justification for the exception.
* **Regular Key Rotations**: Ensuring that the keys, whether managed by us or the CSP, undergo regular rotations, diminishes potential security risks.
* **Training and Awareness**: Periodic training sessions for our staff ensure they are well-versed with the nuances of encryption and the significance of key management in our cloud strategy.
