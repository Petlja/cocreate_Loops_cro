# Skytale

The Skytale (skytale) is one of the oldest known tools for encryption, dating back to ancient Greece around 400 BC. It was a simple cylindrical device used by the Spartans to send secret messages during military campaigns.

A strip of parchment or leather was wrapped around a wooden rod (*skytale*) of a certain diameter. The message was then written lengthwise across the wrapped strip. To decrypt, the receiver wrapped the strip around a rod of the same diameter and read the message lengthwise, the same way it was written.

If you want to encrypt the message:

```text
attackatdawn
```

and you choose a rod that allows **3 letters per wrap**, the strip goes around it 4 times. You write the message along the rod, row by row, 4 letters per row (one on each wrap), forming a table:

```text
a t t a
c k a t
d a w n
```

The encrypted text is then obtained by reading column by column (this is the order of the letters on the unwound strip):

```text
acdtkatawatn
```

To decrypt the message, the receiver wraps the strip around a rod of the same diameter and reads row by row again to reconstruct the original message.

## First assignment

Create a console application in any programming language to encrypt and decrypt messages using the Skytale cipher.

The allowed alphabet for messages contains only lowercase letters of the English alphabet:

```text
Σ = { a, b, c, d, e, f, g, h, i, j, k, l, m, n, o, p, q, r, s, t, u, v, w, x, y, z }
```

Spaces, uppercase letters, numbers, and other characters are not allowed!

In the first line of input there is a message `m` of at most one hundred characters. In the second line there is an integer `k` (the number of columns in the table for encryption). In the third line there is an integer `s` (1 for encryption, 2 for decryption).

### Test Example 1

If the input is:

```text
attackatdawn
4
1
```

the output should be:

```text
acdtkatawatn
```

### Test Example 2

If the input is:

```text
acdtkatawatn
4
2
```

the output should be:

```text
attackatdawn
```

## Solution hints

For **encryption**, write the plaintext row by row in a table with `k` columns. Read the table column by column to get the ciphertext.

For **decryption**, write the ciphertext column by column into a table with `k` columns (each column holds the message length divided by `k` letters), then read the table row by row to reconstruct the plaintext.

## More complex Skytale Assignments (optional)

### Expand the allowed alphabet

Include uppercase letters, spaces, numbers, and punctuation marks.

### Use functions

Create `encrypt()` and `decrypt()` functions to make the code modular.

### Create a class

Implement a `SkytaleCipher` class that stores `k` and provides methods for encryption and decryption.

### Encrypt and decrypt files

Modify the program so that it reads plaintext or ciphertext from a file and writes the result to another file.

### Handle incomplete rows

Modify the program so that if the last row is shorter than `k`, it still encrypts and decrypts correctly, handling incomplete rows appropriately.
