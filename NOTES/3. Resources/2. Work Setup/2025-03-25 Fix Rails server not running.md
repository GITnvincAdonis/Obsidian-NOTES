---
creation date: <% tp.file.creation_date() %>
---

> [!Danger] Reason for failing

When a terminal closes abruptly, the server still runs in the background, on a temp file.
When enter the rails server command and the following errors shows up:

```
started with pid 14085
12:19:51 css.1  | started with pid 14086
12:19:52 web.1  | => Booting Puma
12:19:52 web.1  | => Rails 8.0.2 application starting in development 
12:19:52 web.1  | => Run `bin/rails server --help` for more startup options
12:19:52 web.1  | A server is already running (pid: 11058, file: /home/raveon/Documents/code/shoponline-rails/tmp/pids/server.pid).
12:19:52 web.1  | Exiting
12:19:52 web.1  | exited with code 1
12:19:52 system | sending SIGTERM to all processes
12:19:52 css.1  | bin/rails aborted!
12:19:52 css.1  | SignalException: SIGTERM (SignalException)
12:19:52 css.1  | 
12:19:52 css.1  | Tasks: TOP => tailwindcss:watch
12:19:52 css.1  | (See full trace by running task with --trace)
12:19:52 css.1  | exited with code 1
```


The server needs to be killed. Use the following command:

```
kill -9 *pid in the error shown. In this case: 11058*
```

Link to original: [[2025-03-25]]