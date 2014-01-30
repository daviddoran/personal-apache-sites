# Personal Apache Sites

This is a repo for the Apache site configs for my personal sites and
side-projects; a way to track the VirtualHosts and SSL configs in Git.

I use an rsync script to sync tracked files to the server so updating
the configs is even easier than SSHing in and editing them on the server.

## SSL Ciphersuite

After researching a few alternatives for the perfect SSL ciphersuite
(the set of SSL ciphers the server will use to encrypt the connection)
I came across the [Mozilla Recommended Ciphersuite](https://wiki.mozilla.org/Security/Server_Side_TLS#Recommended_Ciphersuite).

When implemented on daviddoran.com and three.daviddoran.com this ciphersuite
earned an A+ on the [Qualys SSL Labs test](https://www.ssllabs.com/ssltest/analyze.html?d=daviddoran.com).

Unless you can think of a reason not to I'd highly recommend following their advice.

## Relative Paths

It's unfortunate that (as far as I know) Apache 2.4 still doesn't support
using paths relative to the current config file. This would be helpful for
the paths to the config includes and the SSL files (certs, keys, chain files).

I'd be interested to hear if there are any ways to avoid absolute paths.
