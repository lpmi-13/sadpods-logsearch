# Sadpods Logsearch

Inspired by the great work at [Sad Servers](https://sadservers.com), this is an implementation of the "Saskatoon" activity in Gitpod, where you need to search through some webserver logs and parse them for different questions.

## Running in Gitpod

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/lpmi-13/sadpods-logsearch)

Even though this is a very simple task that you could just run locally, if you're in a windows environment and have no easy way to run the commands, then you can just open this in Gitpod.

Othewise, running the commands locally is perfectly fine.

## The task

There are some server access logs called `access.log`. You will need to parse them to answer a few questions.

1) What is the most common IP address that shows up in the logs? When you find it, add the number of requests from this IP to `results.txt`.

2) How many of the requests from the most common IP are `GET` requests? When you find that number, add that to the next line in `results.txt`.

3) This IP address is sending requests from a bunch of different User Agents. Find the User Agent that's used the most frequently, and get the total number of requests from the most common IP with that User Agent. When you find that number, add it to the third line in `results.txt`.

## Checking your answer

If, for example, the number of requests from the most common IP is 54...and the number of `GET` requests from that IP is 100...and the most frequent User Agent is `Mozilla/5.0 (Windows NT 6.3; rv:64.0) Gecko/20100101 Firefox/64.0` used 18 times...

Then the file `requests.txt` should look like:

```
54
100
18
```

> The numbers above are only as examples, they are not the real answers.

Once you've put the three answers into the file, you can check them by calculating the MD5 message digest of the file with `md5sum results.txt`.

The result should be `5614254895e34ba8fa673796e0523f67`.
