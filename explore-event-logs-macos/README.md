<h1>
  <span class="headline">Event Logs Lab</span>
  <span class="subhead">Explore Event Logs - macOS</span>
</h1>

## Background

Starting with OS X 10.12 Sierra, macOS has used a unified logging system to capture events from the operating system, applications, and other sources. The Console app is the primary tool for viewing and working with these logs.

Some key log sources include:

- **system.log:** The primary system log. It records events from the OS, kernel, and many system processes.

- **appname.log:** Each application can write to its own log, named after the application. Useful for app-specific issues.

- **accountpolicy.log:** Contains events related to login attempts, account lockouts, password policies, and so on. It's essential for security auditing.

Other logs capture events from specific subsystems like WiFi, Bluetooth, iCloud, and Time Machine. The Console app lets you view these logs, filter and search entries, and save queries for notable events.

## Accessing the logs

Open the Console app (Applications > Utilities > Console) or search for `Console` using Spotlight (<kbd>Cmd</kbd> + <kbd>Space</kbd>). In the left sidebar, click on the Mac listed under **Devices**.

Browse the different log categories like Crashes, Security, Applications, and so on. Select the **All Messages** log under the **Files** section - this shows a unified view of all log entries.

Here are some tips for navigating the **Console** app:

- Use the search bar to filter the log entries.

- Try a simple text search for error to see all log entries with `error` in the message.

- Click the **+** button next to the search bar for more advanced filtering options.

- Double-click a log entry to see its full details in a separate pane.

- Right-click a log entry and choose **Reveal in Log** to open the specific log file containing that entry.

- Explore the crash reports in the **Crash Reports** > **User** section

## Example events to look for

**system.log:**

- Kernel panics: "panic(cpu 2 caller 0xffffff80023ad88d)".
- Disk errors: "disk0s2: I/O error".

**accountpolicy.log:**

- Failed logins: "Failed to authenticate user".
- Account lockouts: "Account locked for user".

**Crash reports:**

- Look for any crash reports for critical applications.
- Note the **Exception Type** and **Exception Codes** fields, which can help identify the cause of the crash.

## Take a screenshot of your Console application

Take a screenshot of the Console application showing some of the logs you explored.

Add the screenshot to your <code class="filepath">README.md</code> file in the **Screen capture of your operating system's event viewer** section. You may need to look up how to do this online or ask an AI assistant.

## Reflection

Answer any one of the following questions in the **Reflection** section of your <code class="filepath">README.md</code> file:

- How might you use **Console** to investigate a reported problem with a Mac?
- What types of events would you review to assess the general health and security of a Mac?
- How could you automate alerts for critical events like kernel panics or security breaches?

The Console app and unified logging system provide deep insights into the workings of macOS and its applications. Taking time to get familiar with its structure and capabilities will pay dividends when you need to diagnose tricky issues or proactively monitor a fleet of Macs. Keep exploring the logs to see what other insights you can uncover!
