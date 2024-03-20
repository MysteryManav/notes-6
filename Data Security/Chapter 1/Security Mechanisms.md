- **Specific Security Mechanisms**: Integrated into appropriate protocol layer in order to provide some OSI security services:
	1. **Decipherment**: Hiding or Covering data using mathematical algorithms
	2. **Digital Signatures**: Sender can electronically sign the data and the receiver can electronically verify the signature
	3. **[[Access Control]]**: A variety of mechanisms that enforce access rights to resources
	4. **[[Data Integrity]]**: A variety of mechanisms used to assure the integrity of a data unit or stream of data units
	5. **[[Authentication|Authentication Exchange]]**: Two entities exchange some messages to prove their identity to each other
	6. **Traffic Padding**: Insertion of bits into gaps in a data stream to frustrate traffic analysis attempts
	7. **[[Introduction - Security Services#^2c6c66|Routing Control]]**: Selecting and Continuously changing routes between sender and receiver to prevent opponent from eavesdropping
	8. **Notarization**: The use of a trusted third party to assure and control the communication

- **Persuasive Security Mechanism**: Not integrated to any particular OSI security service or protocol layer:
	1. **Trusted Functionality**: That which is perceived to be correct w.r.t some criteria
	2. **Event Detection**: Detection of security relevant events
	3. **Security Label**: Marking bound to resource that names or designates the security attributes of that resource
	4. **Security Recovery**: Deals with requests from mechanisms, such as event handling and management functions and takes recovery actions
