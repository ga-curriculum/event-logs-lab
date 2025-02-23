<h1>
  <span class="headline">Event Logs Lab</span>
  <span class="subhead">Exploring Windows Logs</span>
</h1>

The goal of this hands-on lab is for you to gain experience navigating and analyzing the built-in Windows Event Logs. You'll learn where to access key logs, how to filter log entries to find relevant information, and practice identifying potential issues in the logs. Building skill in interpreting these native Windows logs is valuable for troubleshooting and monitoring the health of your systems.

## Background

Windows Event Logs are a centralized repository for logging messages from the operating system, applications, and other sources. Different logs capture events from various parts of the system:

- **Application Log:** Contains events logged by applications and programs. Helpful for troubleshooting software issues.

- **System Log:** Records events from Windows system components, like driver failures or other system issues.

- **Security Log:** Logs events like successful and failed logins, access to resources, and changes to security policies. Crucial for identifying potential security breaches.

Other logs, like the Setup, Forwarded Events, and individual application logs provide additional insights. Regularly reviewing key logs helps you proactively spot emerging problems, investigate issues, and audit system activities.
Steps

## Accessing the Logs

- Open the Event Viewer:
  - Press Win + R to open the Run dialog
  - Type eventvwr.msc and press Enter

- In the left pane, expand "Windows Logs"

- Click on each of the following logs to select it:

  - Application
  - System
  - Security

- For each log, click on "Filter Current Log" in the Actions pane on the right

- In the filter dialog, choose a time range like the last 24 hours, then click OK to apply the filter

- Review the filtered log entries, looking at:

  - The Level (Information, Warning, Error)
  - The event Source and Event ID
  - The general description of the event

If you see an interesting or concerning event, double-click it to open the event properties window with more details
Check the Application and Services Logs for events from specific programs or Windows components

## Example Events to Look For

**Application Log**

- Event 1000 from source Application Error - indicates an application crash
Warnings or errors from specific applications you use

**System Log**

- Event 7001 - A service did not start due to an error
- Event 41 - The system rebooted without cleanly shutting down first
- Driver errors - e.g. Event 219 from NTFS: "The driver detected a controller error on DeviceSCSI0"

**Security Log**

- Event 4624 - Successful login
- Event 4625 - Failed login
- Event 4720 - A user account was created
- Event 4724 - An attempt was made to reset an account's password

## Reflection

Think about the following as you work with the Event Logs:

- How can reviewing these logs help you identify and troubleshoot issues?

- What types of events would you want to check on a regular basis?

- How might you automate checking for certain notable events?

Remember, the Event Logs are just one source of system information, but they're a powerful one. Get comfortable navigating them, filtering them, and interpreting the different types of events. Building this foundational skill will serve you well in many troubleshooting and monitoring scenarios!
