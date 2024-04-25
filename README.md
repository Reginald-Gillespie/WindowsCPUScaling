# WindowsCPUScaling
Automatically scale CPU frequency using windows power profiles based on whether computer is plugged in or not.

# Setup
Put these three files in a folder somewhere, I use `Document\Scripts`

Then, open windows Task Scheduler, create a new task. 

Under `Triggers`, click New, set `Begin the task` to `On an Event`. Set `Log` to `System` and `Event ID` to `105`.

Under `Actions`, add a new action and specify the location of `PowerChanged.ps1`. 

Under `Conditions`, uncheck `Start the task only of the computer is on AC power.`

Then edit the bottom of `PowerChanged.ps1` to point to where the two other scripts are located.

If there is any interest I'll make a setup script to create the task.

## Other
You can see all windows power profiles by running `powercfg /l`. Some beefy computers might have an `Ultra Performance` option, which you can put the profile ID for in `performance.ps1`.
