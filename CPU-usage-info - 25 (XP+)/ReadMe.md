This example shows current CPU usage in percents (0-100) on the progress-bar, and it uses the "CallbackCtrl.dll" because this version of InnoSetup does not have the "CreateCallback" function. But, "CallbackCtrl.dll" is not needed from version v6.0, so, it's used only in versions of InnoSetup below v6.0.
You can change the refresh speed by clicking on buttons close to the progress-bar (from 100ms to 1000ms).