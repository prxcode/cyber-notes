# Users & Groups
### Understanding Users
Every user has a <username>, UID, and associated home directory.

### Important Files
- `/etc/passwd`: User account info.
- `/etc/shadow`: Encrypted passwords.

### Adding & Removing Users
- `adduser <username>`: Adds a user
- `deluser <username>`: Deletes a user
- `passwd <username>`: Set/change password

### Group Management
- `groupadd`: Add a new group
- `usermod -aG group user`: Add user to a group
- `groups user`: Show user's groups