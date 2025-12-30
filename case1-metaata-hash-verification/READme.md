# *Case 1: Metadata & Hash Verification — Tampered File Investigation*

## *Scenario*
This investigation was conducted to verify the integrity of digital evidence by comparing cryptographic hash values of original and modified files including images and documents.

## *Evidence Examined*
### *Image Files*
- Original-img.jpg  
- Edited-img.jpg  
- WhatsApp-shared.jpg  
- Email-shared.jpg  

### *Document Files*
- Report-original.docx  
- Report-edited.docx  

## *Tools Used*
- Hash Generator (MD5, SHA-1, SHA-256)
- Manual file integrity comparison

## *Methodology*

### *1. Evidence Collection*
Original and edited versions of image and document files were collected without altering their content.

### *2. Hash Generation*
MD5, SHA-1 and SHA-256 hash values were generated for each file.

### *3. Integrity Comparison*
Hash values of original files were compared against their edited and shared counterparts.

## *Hash Analysis Summary*

| File | MD5 | SHA-1 | SHA-256 |
|-----|------|------|--------|
| Original-img.jpg | `0b48f4a6c745f4887752cdaac1229452` | `0bec2eb0e3ad98c03570d8393b9d569910ae0dda` | `b8b6c8828205bc17be3d44dc70047b9e140f8c2a8ea170cd7295c756e47ea9f7` |
| Edited-img.jpg | `38e2faf2030c360e891033b377f2fb2a` | `13b2a18514a2521593d1b8df2456f0882535166b` | `fc9fa10c48c442ab9af1f77f8fa9f5ba3f7a887cb4d8bd90603f8c2aef3c7251` |
| WhatsApp-shared.jpg | `0b48f4a6c745f4887752cdaac1229452` | `0bec2eb0e3ad98c03570d8393b9d569910ae0dda` | `b8b6c8828205bc17be3d44dc70047b9e140f8c2a8ea170cd7295c756e47ea9f7` |
| Report-original.docx | `e42244250ef8c64e2ed267eeaac89ba6` | `1c9be5ac1ba080cc333ba0ee7da77a4e8c3adeda` | `a83669d400b29c6314834a29164d2408851ba8d9b48a06e4420ba317a47346b3` |
| Report-edited.docx | *(hash differs from original)* | *(hash differs from original)* | *(hash differs from original)* |

## *Screenshots / Evidence*

### *Original Image*
![Original](images/original-img.jpg)

### *Edited (Tampered) Image*
![Edited](images/edited-img.jpg)

## *Integrity Interpretation*
The original image and its WhatsApp and Email shared copies produced identical hash values, indicating that no content modification occurred during transmission.
The edited image produced completely different hash values, confirming tampering.
This validates:
- Transmission does not necessarily alter file integrity  
- Any content modification is immediately reflected in cryptographic hashes

## *Key Findings*
- Hash values of original and edited files were completely different.
- Even minimal changes in file content resulted in new cryptographic hashes.
- Files shared through email and WhatsApp retained original hashes due to compression handling.

## *Observations*
- Editing or modifying any file alters its cryptographic hash.
- Hash verification is a reliable method for detecting tampering.
- File transmission methods may preserve original integrity but still require verification.

## *Learning Outcome*
- Learned generation and application of MD5, SHA-1 and SHA-256.
- Understood file integrity verification in digital forensics.
- Gained practical experience with real-world evidence validation.

## *Evidence Relationship*
The same original image file was transmitted through different channels for analysis:
- *Original-img.jpg* → Original source file  
- *WhatsApp-shared.jpg* → Same file sent via WhatsApp  
- *Email-shared.jpg* → Same file sent via Email  
These versions were compared against an intentionally modified file:
- *Edited-img.jpg* → Tampered version of the original image

## *Conclusion*
Hashing proved to be a highly reliable technique for verifying file integrity.  
This case demonstrates how digital modifications are immediately reflected in cryptographic hash values, making hashing a fundamental tool in forensic investigations.

## *Skills Demonstrated*
Digital evidence handling, cryptographic hashing, integrity verification, forensic documentation, investigative reporting
