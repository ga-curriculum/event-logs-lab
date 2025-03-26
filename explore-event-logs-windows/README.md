<h1>
  <span class="headline">Event Logs Lab</span>
  <span class="subhead">Explore Event Logs - Windows</span>
</h1>

## Background

Windows Event Logs are a centralized repository for logging messages from the operating system, applications, and other sources. Different logs capture events from various parts of the system:

- **Application log:** Contains events logged by applications and programs. Helpful for troubleshooting software issues.

- **System log:** Records events from Windows system components, like driver failures or other system issues.

- **Security log:** Logs events like successful and failed logins, access to resources, and changes to security policies. This log is crucial to help identify potential security breaches.

Other logs, like the **Setup**, **Forwarded events**, and individual application logs, provide additional insights. Reviewing key logs helps you proactively spot emerging problems, investigate issues, and audit system activities.

## Accessing the logs

Open the **Event Viewer** application:

- Press <kbd>Win</kbd> + <kbd>R</kbd> to open the Run dialog.
- Type `eventvwr.msc` and press <kbd>Enter</kbd>.

In the left pane, expand **Windows Logs**.

Here are some tips for navigating the **Event Viewer** app:

- Click on each of the following logs to select it:

  - **Application**
  - **System**
  - **Security**

- For each log, select **Filter Current Log** in the **Actions** pane on the right.

- In the filter dialog, choose a time range like the last 24 hours, then select **OK** to apply the filter.

- Review the filtered log entries, looking at:

  - The Level (Information, Warning, Error).
  - The event Source and Event ID.
  - The general description of the event.

If you see an interesting or concerning event, double-click it to open the event properties window with more details.

Check the **Application and Services Logs** for events from specific programs or Windows components.

## Example events to look for

**Application Log:**

- Event 1000 from source Application Error - indicates an application crash.

**System Log:**

- Event 7001 - A service did not start due to an error.
- Event 41 - The system rebooted without cleanly shutting down first.
- Driver errors - For example, Event 219 from NTFS: `The driver detected a controller error on DeviceSCSI0`.

**Security Log:**

- Event 4624 - Successful login.
- Event 4625 - Failed login.
- Event 4720 - A user account was created.
- Event 4724 - An attempt was made to reset an account's password.

## Take a screenshot of your Event Viewer application

Take a screenshot of the Event Viewer application showing some of the logs you explored.

Add the screenshot to your <code class="filepath">README.md</code> file in the **Screen capture of your operating system's event viewer** section. You may need to look up how to do this on the internet.

## Reflection

Answer any one of the following questions in the **Reflection** section of your <code class="filepath">README.md</code> file:

- How can reviewing these logs help you identify and troubleshoot issues?
- What types of events would you want to check on a regularly?
- How might you automate checking for certain notable events?

Remember, the Event Logs are just one source of system information, but they're powerful. Get comfortable navigating, filtering, and interpreting different types of events. Building this foundational skill will serve you well in many troubleshooting and monitoring scenarios!
