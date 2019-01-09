# EasySafe attack sketch
## Read contents of encrypted page in filesystem

Adversary model: Blind

Complexity: K + P

## Method
The attacker brute forces the passphrase and learn the FSID through trial and error by attempting each candidate passphrase against every encrypted file to determine if that file is the configuration file.

The attacker does not possess any revision tags. So the attacker repeats this trial-and-error method against all pages of the filesystem to locate inode tables. The attacker can then read the file contents.