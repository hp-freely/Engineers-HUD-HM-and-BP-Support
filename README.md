# Engineers HUD HM and BP Support
Adds HudManager and BuddyPoints support for the Engineers HUD

### Summary
The final version of the original Engineers HUD was released in 2002. This makes the script very old, and it means that it was developed before many other scripts existed, including common support scripts.

One support script that did not yet exist at that time was HudMover, which allows users to move HUDs to their desired position by mouse. Instead, this script forced users to actually input the X and Y position of the HUD in order to place it exactly where they wanted.

The script also supported dynamically moving the Chat HUD out of the way at certain times. I have no idea what the context of this is, but that's certainly something we don't want to happen these days.

Another script that may not yet of existed was BuddyPoints. BuddyPoints adds a right-menu option for adding a buddy point to a player. It did so by dynamically adding the option to the end of that menu. EngineerHud also adds a right-menu option called "Find Player". However, EH did *not* dynamically add that option.  Rather, it forced that option to a specific index.

The above caused a conflict. If BuddyPoints loaded first, and then EH loaded second, then EH would overwrite the BuddyPoint menu option.

Given the above context, I have taken the following actions:
1. I have added HUDMover support.
2.) I have added code to dynamically add "Find Player" and "Find Object" menu items in EH, so that it does not conflict with BuddyPoints.
3. I have commented out all code associated with manually setting the X and Y position of the HUD
4. I have commented out all code associated with moving the Chat HUD

Explicitly regarding #2 and #3, I have *not* removed any code. I have simply commented code out. 
