# Simple Encryption and Decryption

## Simple file/stream encryption and decryption using OpenSSL

Create and store a 32-byte base64 random encryption key named `secret`:

```
./mkkey secret
```

Encrypt the contents of `file` with the `secret` key and write it to `file.enc`:

```
./encrypt secret < file > file.enc
```

Decrypt the contents of `file.enc` to standard output:

```
./decrypt < file.enc
```

Keys are stored in `~/.keys` by default. Set the `KEY_DIR` environment variable to specify a different location.


## Credit
This Encryption and Decryption script is slightly modifed version of https://gist.github.com/sstephenson/5368148

Significant changes:
- Use a base64 characters for key
- Random key file generation is set to 32-byte
