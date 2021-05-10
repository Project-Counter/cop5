.. The COUNTER Code of Practice Release 5 © 2017-2021 by COUNTER
   is licensed under CC BY-SA 4.0. To view a copy of this license,
   visit https://creativecommons.org/licenses/by-sa/4.0/

Double-Click Filtering
----------------------
The intent of double-click filtering is to remove the potential of over-counting which could occur when a user clicks the same link multiple times, typically due to a slow internet connection. Double-click filtering applies to Total_Item_Investigations, Total_Item_Requests, No_License and Limit_Exceeded. See :numref:`unique-items` and :numref:`unique-titles` below for information about counting unique items and titles. The double-click filtering rule is as follows:

Double-clicks, i.e. two clicks in succession, on a link by the same user within a 30-second period MUST be counted as one action. For the purposes of COUNTER, the time window for a double-click on any page is set at a maximum of 30 seconds between the first and second mouse clicks. For example, a click at 10:01:00 and a second click at 10:01:29 would be considered a double-click (one action); a click at 10:01:00 and a second click at 10:01:35 would count as two separate single clicks (two actions).

A double-click may be triggered by a mouse-click or by pressing a refresh or back button. When two actions are made for the same URL within 30 seconds the first request MUST be removed and the second retained.

Any additional requests for the same URL within 30 seconds (between clicks) MUST be treated identically: always remove the first and retain the second.

There are different ways to track whether two requests for the same URL are from the same user and session. These options are listed in order of increasing reliability, with Option 4 being the most reliable.

#. If the user is authenticated only through an IP address, that IP address combined with the browser’s user-agent (logged in the HTTP header) MUST be used to trace double-clicks. Where you have multiple users on a single IP address with the same browser user-agent, this can occasionally lead to separate clicks from different users being logged as a double click from one user. This will only happen if the multiple users are clicking on exactly the same content within a few seconds of each other.
#. When a session cookie is implemented and logged, the session cookie MUST be used to trace double-clicks.
#. When a user cookie is available and logged, the user cookie MUST be used to trace double-clicks.
#. When an individual has logged in with their own profile, their username MUST be used to trace double-clicks.
