<h1>
  <span class="headline">Event Logs Lab</span>
  <span class="subhead">Explore Event Logs - Ubuntu</span>
</h1>

## Background

Starting with Ubuntu 17.10, Ubuntu has used the **Logs** application to capture events from the operating system, applications, and other sources.

Some key log sources include:

- <code class="filepath">/var/log/auth.log</code>: Keeps track of authentication events, including logins, failed login attempts, and `sudo` usage. This log is crucial for security auditing and monitoring user access.

- <code class="filepath">/var/log/debug</code>: Provides detailed debugging information about the system and the applications running on it. If something is not working as expected, this log can help you identify the issue.

- <code class="filepath">/var/log/syslog</code>: Contains other logs related to your system. Check here if you can't find the log you're looking for in another location, check here.

Other logs capture events from specific subsystems like the Linux kernel at <code class="filepath">/var/log/kern.log</code> or details about background processes in the <code class="filepath">/var/log/daemon.log</code> log. The **Logs** app lets you view these varied logs in one place.

## Accessing the logs

Start by opening the **Logs** app using the system search.

Select a log file from the left sidebar to view its contents. If no logs are visible in the left sidebar of the **Logs** app, select the **gear** icon in the top right corner of the screen to open one of the log files discussed above.

Here are some tips for navigating the **Logs** app:

- If a log file is displayed in bold text on the left sidebar, it means that there have been new entries in that log file since you last opened it.

- You're able to monitor the logs in real-time. New additions to a log file are displayed with bold text in the main window as they occur.

- Use the **magnifying glass** icon in the top right corner of the screen to open the search prompt to help find a specific log entry.

- Try a simple text search for error to see all log entries with 'error' in the message.

## Example events to look for

<code class="filepath">/var/log/auth.log</code>:

- Authentication failures: `Failed password for user from location`.
- Successful logins: `Accepted password for user from location`.
- `sudo` usage: `user : TTY=pts/0 ; PWD=directory ; USER=root ;COMMAND=command run`.

<code class="filepath">/var/log/debug</code>:

- Application crashes: `application crashed with signal`.
- Ubuntu system errors: `systemd[1]: Failed to start service`.

## Take a screenshot of your Logs application

Take a screenshot of the **Logs** application showing some of the logs you explored.

Add the screenshot to your <code class="filepath">README.md</code> file in the **Screen capture of your operating system's event viewer** section. You may need to look up how to do this online or ask an AI assistant.

## Reflection

Answer any one of the following questions in the **Reflection** section of your <code class="filepath">README.md</code> file:

- How might you use the **Logs** app to investigate a reported problem with an Ubuntu system?
- How could you use the logs to monitor system performance or security?
- How could you automate alerts for critical events like kernel panics or security breaches?
