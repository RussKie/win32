---
Description: 'Presents the steps to decrypt an encrypted message.'
ms.assetid: '6af7dd28-325e-431a-9cdb-109d93af6302'
title: Decrypting Data
---

# Decrypting Data

This section presents the steps to decrypt an encrypted message.

**To decrypt an encrypted message**

1.  Get a pointer to the digitally enveloped message.
2.  Open a certificate store.
3.  From the message, retrieve the recipient identifier (My ID).
4.  Use the recipient identifier to retrieve the certificate.
5.  Get the private key for the certificate.
6.  Use the private key to decrypt the symmetric (session) key.
7.  Retrieve the encryption algorithm from the message.
8.  Using the decrypted session key and the encryption algorithm, decrypt the data.

[**CryptDecryptMessage**](cryptdecryptmessage.md) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.

**To decrypt data using CryptDecryptMessage**

1.  Get a pointer to the encrypted BLOB.
2.  Open a certificate store.
3.  Create a certificate store array.
4.  Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](crypt-decrypt-message-para.md) structure.
5.  Call [**CryptDecryptMessage**](cryptdecryptmessage.md) to decrypt the data contained in the message.

[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented. Comments show which code elements accomplish each step in the procedure. For details about the function, see [**CryptDecryptMessage**](cryptdecryptmessage.md), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](crypt-decrypt-message-para.md).

 

 


