# lxd-forward
A script created to portforward lxc containers managed by lxd. This script is created by [sokkalf](https://github.com/sokkalf)

Link to blogpost of ussage by sokkalf https://ugle-z.no/articles/2016-09/simplifying-port-forwarding-with-LXD.html?utm_source=pocket_mylist


Adding a rule

Let’s say you have an SMTP server running in a container named ‘mailbox’. To forward port 25 on the container to port 25 on the host, just do this:

```
$ lxd-forward add mailbox 25
```

Another example, what if you have a web server running in the container ‘tomcat’, on port 8080, and want it forwarded to port 80 on the host?

```
$ lxd-forward add tomcat 8080 80
```

Listing rules

To list rules, simply type:
```
$ lxd-forward list
```

Sample output:

```
Rule #  LXD     IP              Host    Container
2       kolab   172.29.46.196   143     143
```

Deleting a rule

To delete a rule, get the rule number from the ‘list’ command, e.g. 2, and do:

```
$ lxd-forward delete 2
```
