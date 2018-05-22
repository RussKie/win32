---
Description: 'Explains how to create a CALG\_SSL3\_SHAMD5 hash.'
ms.assetid: 'dad6fc7f-8abd-4f90-b3e4-8d0169e95087'
title: 'Creating a CALG\_SSL3\_SHAMD5 Hash'
---

# Creating a CALG\_SSL3\_SHAMD5 Hash

**To create a CALG\_SSL3\_SHAMD5 hash**

1.  Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](security.s_gly#-security-secure-hash-algorithm-gly) [*hash*](security.h_gly#-security-hash-gly) of the target data.
2.  Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost. This results in a 36-byte value (16 bytes + 20 bytes).
3.  Get a handle to a [*hash object*](security.h_gly#-security-hash-object-gly) by calling [**CryptCreateHash**](cryptcreatehash.md) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.
4.  Set the hash value with a call to [**CryptSetHashParam**](cryptsethashparam.md). The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter. Calling [**CryptHashData**](crypthashdata.md) using the handle returned by [**CryptCreateHash**](cryptcreatehash.md) in step 3 will fail.
5.  Call [**CryptSignHash**](cryptsignhash.md) to generate the signature.
6.  Call [**CryptDestroyHash**](cryptdestroyhash.md) to destroy the hash object.

 

 


