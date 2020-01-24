

Using either [PuTTY][10] ([see also][20]) or [git bash][30] please connect using `ssh` to the host 
`saskia`.

The full hostname is `saskia.igm.rit.edu`

Use your RIT ID as the username. Use the password given to you.

In PuTTY you will have to fill in the username and hostname separately.

In git-bash you'll issue a command something like this:

```
$ ssh djaigm@saskia.igm.rit.edu
```

Where instead of `djaigm` you will use your own username befoe the `@`


You should, at your earliest convenience, change the password from the one 
given to you. This is done by logging on as above, then issuing the `passwd` 
command.

When you do so, you will be prompted for the existing password (that is, the 
one that was given to you) and then you will be prompted to enter a new 
password, and then to enter it again to confirm.

If you get an error trying to change the password, try again. 

When you succeed changing the password, log out and back in to double-check 
on the change. Then, at your earliest opportunity, commit your password to 
your password management system (if, in fact, you did not use a password 
manager to generate and store the password already in the first place).

[10]: https://www.chiark.greenend.org.uk/~sgtatham/putty/
[20]: https://en.wikipedia.org/wiki/PuTTY
[30]: https://gitforwindows.org/

