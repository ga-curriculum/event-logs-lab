<h1>
  <span class="headline">Event Logs Lab</span>
  <span class="subhead">Explore macOS Event Logs</span>
</h1>

In this lab, you'll get hands-on practice working with some key system logs in macOS. The goal is to familiarize yourself with where to find important logs, how to search and filter log entries, and gain experience spotting notable events that could indicate issues. Building comfort with the native macOS log tools and structure is a valuable skill for supporting and troubleshooting Mac systems.

## Background

Starting with OS X 10.12 Sierra, macOS has used a unified logging system to capture events from the operating system, applications, and other sources. The primary tool for viewing and working with these logs is the Console app.

Some key log sources include:

- **system.log:** The primary system log, records events from the OS, kernel, and many system processes.

- **appname.log:** Each application can write to its own log, named after the application. Useful for app-specific issues.

- **accountpolicy.log:** Contains events related to login attempts, account lockouts, password policies, etc. Important for security auditing.

Other logs capture events from specific subsystems like WiFi, Bluetooth, iCloud, and Time Machine. The Console app lets you view these varied logs, filter and search entries, and save queries for notable events.

## Accessing the logs

- Open the Console app (Applications > Utilities > Console)

- In the left sidebar, click on the Mac listed under "Devices"

- Browse the different log categories like Crashes, Security, Applications, etc.

- Click on the "All Messages" log under the Files section - this shows a unified view of all log entries

- Use the search bar to filter the log entries

- Try a simple text search for error to see all log entries with 'error' in the message

- Click the "+" button next to the search bar for more advanced filtering options

- Double-click a log entry to see its full details in a separate pane

- Right-click a log entry and choose "Reveal in Log" to open the specific log file containing that entry

- Explore the crash reports in the Crash Reports > User section

## Example events to look for

**system.log**

- Kernel panics: "panic(cpu 2 caller 0xffffff80023ad88d)"
- Disk errors: "disk0s2: I/O error"

**accountpolicy.log**

- Failed logins: "Failed to authenticate user"
- Account lockouts: "Account locked for user"

**Crash reports**

- Look for any crash reports for critical applications
- Note the "Exception Type" and "Exception Codes" fields which can help identify the cause of the crash

## Reflection

Consider the following as you work with the macOS logs:

- How might you use Console to investigate a reported problem with a Mac?
- What types of events would you review to assess the general health and security of a Mac?
- How could you automate alerts for critical events like kernel panics or security breaches?

The Console app and unified logging system provide deep insights into the workings of macOS and its applications. Taking time to get familiar with its structure and capabilities will pay dividends when you need to diagnose tricky issues or proactively monitor a fleet of Macs. Keep exploring the logs to see what other insights you can uncover!
