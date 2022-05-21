# Caesar_Cypher
## Implementation of the Caesar Cypher in Python

### Here we implement the Caesar cypher by first asking our user to encrypt or decrypt a message and obtain the encryption offset. We then ask for the message to encrypt (and convert to lower case for simplicity.

### By encrypting, we take the user's message and convert each alphabetic character in the message into it's ASCII value. We add the offset to each ASCII value. If adding our offset exceeds the lower case values in ASCII, 97-122, we subtract 26 from the value to bring it back in. This essentially creates a circular alphabet: 'z' + 1 = 'a'.

asc = ord(character)
new_asc = asc + offset
if new_asc > 122:
    new_asc -= 26
elif new_asc < 97:
    new_asc += 26

return chr(new_asc)

### Decryption follows this same logic, though we multiply the inputted offset by -1 to reverse encryption.
