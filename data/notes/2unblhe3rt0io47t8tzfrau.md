
nohup
```
Using nohup <command> & executes command in the background 
so that you can continue to use your shell. You can use jobs -l to 
see the process identifier (PID), which will let you bring the 
process to the foreground or terminate it. nohup will redirect 
standard output (stdout) and standard error (stderr) to the file 
nohup.out.
```

httpie
httpie, an awesome command-line HTTP client for testing requests to your web app from the console:

On a VM, At this point in the tutorial, your app is only listening on localhost, which is the address 127.0.0.1. It’s not yet accessible from a browser, but you can still give it its first visitor by sending it a httpie request