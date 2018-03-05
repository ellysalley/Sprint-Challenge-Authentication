## Questions - Self Study - You can exercise your Google-Fu for this and any other _Sprint Challenge_ in the future.

1. Describe Middleware, Sessions (as we know them in express), bcrypt and JWT.

- Middleware is repeated or common functions in between the client and route handler
- Sessions
- bcrypt is a password hashing function.
- JWT(JSON Web Token) is an open, industry standard RFC 7519 method for representing claims securely between two parties. It generates tokens that look for example like this: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJsb2dnZWRJbkFzIjoiYWRtaW4iLCJpYXQiOjE0MjI3Nzk2Mzh9.gzSraSYS8EXBxLN_oWnFSRgCzcmJmMjLiuyu5CSpyHI 


1. What does bcrypt do in order to prevent attacks?

- Generate a random salt. A "cost" factor has been pre-configured. Collect a password.
- Derive an encryption key from the password using the salt and cost factor. Use it to encrypt a well-known string. Store the cost, salt, and cipher text. Because these three elements have a known length, it's easy to concatenate them and store them in a single field, yet be able to split them apart later.
- When someone tries to authenticate, retrieve the stored cost and salt. Derive a key from the input password. Encrypt the same well-known string. If the generated cipher text matches the stored cipher text, the password is a match.
- Bcrypt operates in a very similar manner to more traditional schemes based on algorithms like PBKDF2. The main difference in its use of a derived key to encrypt known plain text; other schemes (reasonably) assume the key derivation function is irreversible, and store the derived key directly.

1. What are the three parts of the JSON Web Token?
- A header, a payload, and a signature. 
