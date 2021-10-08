

Action | Command
---|---
Generate authentication keys | `ssh-keygen -t rsa -b 4096 -C your_email@example.com [-f $HOME/.ssh/id_rsa]`
Connect to destination ignoring known_hosts | `ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no DESTINATION [-p PORT]`

