# LETCOOR 1.0.0 — Complete User Documentation

> Documentation prepared from the actual **LETCOOR 1.0.0** source code provided on October 30, 2026.
> This documentation describes the features actually exposed by the Android/Windows application and the current interface.

---

## Table of Contents

1. [Getting started: connecting devices](#1-getting-started-connecting-devices)
2. [Important permissions, especially offline](#2-important-permissions-especially-offline)
3. [Create or join a group](#3-create-or-join-a-group)
4. [Understanding the main screen](#4-understanding-the-main-screen)
5. [The tactical map](#5-the-tactical-map)
6. [Create a report](#6-create-a-report)
7. [Create an objective](#7-create-an-objective)
8. [Create an order](#8-create-an-order)
9. [Create a rally point](#9-create-a-rally-point)
10. [Send a safety alert](#10-send-a-safety-alert)
11. [Interact with an already published object](#11-interact-with-an-already-published-object)
12. [The “Command and activity” panel](#12-the-command-and-activity-panel)
13. [The group or team menu](#13-the-group-or-team-menu)
14. [Teams](#14-teams)
15. [Participants and roles](#15-participants-and-roles)
16. [Invite a new participant](#16-invite-a-new-participant)
17. [Operations](#17-operations)
18. [Role campaigns](#18-role-campaigns)
19. [Sessions](#19-sessions)
20. [Data sharing between teams](#20-data-sharing-between-teams)
21. [Group and team management](#21-group-and-team-management)
22. [Publication limits](#22-publication-limits)
23. [Location](#23-location)
24. [Notifications](#24-notifications)
25. [Offline maps](#25-offline-maps)
26. [Network connection and offline operation](#26-network-connection-and-offline-operation)
27. [Privacy, locking and recovery](#27-privacy-locking-and-recovery)
28. [Available roles](#28-available-roles)
29. [Preparation tips before an activity](#29-preparation-tips-before-an-activity)
30. [Troubleshooting](#30-troubleshooting)
31. [Quick summary](#31-quick-summary)

---

# 1. Getting started: connecting devices

LETCOOR uses a device-to-device invitation system. An invitation can be transmitted by **QR code**, **link**, system sharing or file depending on the platform.

To maximize the chances of connecting, especially **without Internet access**, prepare both devices before the exchange.

## 1.1 Before scanning the QR code or opening the link

On both devices:

1. Open LETCOOR and keep the application in the foreground during the first connection.
2. Enable **Wi‑Fi**.
3. Enable **Bluetooth**.
4. Accept Android/Windows requests concerning **nearby devices**, Bluetooth, Wi‑Fi Direct or the local network.
5. If Android offers to make the phone visible over Bluetooth, accept during the connection phase.
6. If Android asks you to enable location services to allow radio discovery, enabling it is recommended for compatibility with the phone's proximity APIs.
7. The **camera** is only required to scan a QR code. It is not required if you use a link.

> **Important:** authorizing or enabling Android location services for proximity discovery does not automatically enable sharing your position in LETCOOR. Location sharing is a separate feature and remains disabled until you enable it yourself.

## 1.2 Connection by QR code

### On the inviting device

1. Open the group or team menu by tapping its name at the top left.
2. Open the **Invite** tab.
3. If several destinations are available, choose the **group** or **team** to join.
4. Open **Share invitation**.
5. Select **Show QR code**.
6. Leave the QR code displayed on screen.

A QR code may consist of several parts. LETCOOR cycles through them automatically. You can pause the cycle or manually go to the previous/next part.

### On the invited device

1. On the home screen, choose **Join with an invitation**.
2. Press the QR scan button.
3. Allow camera access if Android/Windows asks for it.
4. Point the camera at the QR code on the other device.
5. If the QR code has several parts, keep the camera pointed at the screen until LETCOOR has read all parts.
6. LETCOOR imports the invitation and prepares a **response**.
7. The invited device then displays a **response link** or **response QR code** to send back to the inviting device.

### Sending the response back to the inviter

On the device that created the invitation:

1. Stay in **Invite**.
2. Open **Receive response**.
3. Scan the response QR code, paste the response link or use the available sharing mechanism.
4. LETCOOR verifies the response and then starts the direct connection.

The application then displays the status of the attempt: proximity preparation, Internet connection, local discovery, connection established or timeout.

## 1.3 Connection by link

The procedure is identical, but without using the camera.

### Inviting device

In **Invite > Share invitation**:

1. Choose **Invitation link**.
2. Press **Copy link** or the share button.
3. Send the link to the other participant.

### Invited device

1. Open **Join with an invitation**.
2. Paste the link into **Invitation to accept**, or use the clipboard button.
3. LETCOOR automatically processes a valid link.
4. Then send the **response link** back to the device inviting you.

### Inviting device

In **Receive response**:

1. Paste the response link or scan the response QR code.
2. LETCOOR verifies the response.
3. The connection starts automatically.

## 1.4 Why is there a response to send back?

The bidirectional flow allows both devices to know the information required for the connection attempt. LETCOOR can then try the available paths and authenticate the peer before admitting it to the group or team.

## 1.5 Admission to the group and team

A valid invitation is signed and targets a destination defined when it is created.

- A group invitation allows the corresponding group to be joined.
- An invitation originating from a team may include access to the **parent group and the inviter's team**.
- The group's private keys or complete history are not placed in the QR code.
- Admission is validated by the LETCOOR protocol after authentication; there is no additional manual validation for a valid invitation unless the admission policy or the space's permissions prevent it.

---

# 2. Important permissions, especially offline

LETCOOR uses several system features. For use without Internet access, proximity permissions are particularly important.

## 2.1 Bluetooth and Wi‑Fi Direct

In **Settings > Permissions**, LETCOOR offers:

- **Bluetooth and Wi‑Fi Direct — Allow**
- **Camera — Allow**
- **Location — Check**

On recent Android versions, LETCOOR may notably request system permissions related to:

- nearby devices;
- Bluetooth scanning;
- Bluetooth connection;
- Bluetooth advertising;
- Wi‑Fi Direct / nearby Wi‑Fi devices;
- local network access on Android versions that require it.

On some older Android versions, Bluetooth/Wi‑Fi discovery may depend on the Android location permission.

## 2.2 Location: two different things

You must distinguish between:

1. **Android system location used by some proximity-discovery APIs.**
2. **Voluntary sharing of your position in LETCOOR.**

You can use LETCOOR without publishing your position on the map. Location sharing is configured separately from the **Location** icon.

## 2.3 Camera

The camera is used only for scanning QR codes. Scanning does not require the microphone.

If camera access is denied:

- use the invitation link;
- or re-enable camera access in the Android/Windows settings.

## 2.4 System notifications

System notifications can be enabled from the LETCOOR notification center. They allow native alerts to be received for certain events when the platform supports it.

---

# 3. Create or join a group

On first launch, if the device does not yet have any group, LETCOOR displays the home screen.

You have two choices:

- **Create a group**
- **Join with an invitation**

## 3.1 Create a group

1. Press **Create a group**.
2. Enter the **Group name**.
3. The name must contain at least 2 characters.
4. Press **Create**.

The creator receives the group administration role and can then create teams, invite participants and manage the space according to the capabilities granted by the Core.

## 3.2 Join a group

1. Press **Join with an invitation**.
2. Import the link or QR code.
3. Follow the invitation/response exchange described at the beginning of this documentation.

## 3.3 Personal No.

Each device has a **Personal No.** displayed during onboarding and in the **Context** tab.

This number serves as a user-readable identifier in the interface. The actual cryptographic identity is based on the LETCOOR device identity, not on this displayed code.

---

# 4. Understanding the main screen

LETCOOR uses a **map-centered interface** rather than a sequence of traditional pages.

## 4.1 Header

At the top of the screen:

- on the left: the **name of the currently selected group or team**;
- the subtitle indicates **Group** or **Team**;
- **Not synchronized** may appear if the context is operating without synchronization;
- a bell opens **Notifications**;
- the **Command** button opens the command and activity panel;
- a badge shows network status: direct Internet, relay, Wi‑Fi Direct, local Wi‑Fi, Bluetooth, LAN, synchronization or connection search.

## 4.2 Central map

The map displays objects authorized in the current context:

- orders;
- reports;
- objectives;
- meeting points / rally points;
- safety alerts;
- team presence;
- exact presence when authorized;
- movements / tracks depending on active permissions and sharing.

## 4.3 Legend

The `?` button displays the legend, including:

- Danger;
- Objective;
- Rally point;
- Team.

## 4.4 Footer

The bottom of the screen indicates:

- the number of active members in the context;
- the number of active objects;
- whether a session is currently active, otherwise your Personal No.

## 4.5 Open the group or team menu

Tap the context name at the top left.

The panel contains the tabs:

- **Context**
- **Teams**
- **Participants**
- **Invite**
- **Operations**
- **Management**
- **Settings**

Some functions appear only if your role has the corresponding permission.

---

# 5. The tactical map

## 5.1 Moving around

The map is operated like a standard touch map: pan and zoom.

## 5.2 Add an object

To publish a spatial object:

1. **Long-press** the desired location.
2. LETCOOR opens **Add here**.
3. Actions authorized for your role are displayed.

Available options are:

- **Report**
- **Objective**
- **Order**
- **Rally point**
- **Safety alert**

Actions not authorized in your context are not displayed.

## 5.3 Geographic shapes

Depending on the object type, LETCOOR allows:

- **Point**;
- **Circular area**;
- **Polygon**;
- **Path**.

For a circular area, the radius can be set from **10 to 500 m**.

For a polygon or path:

1. choose the geometry;
2. press **Draw on map**;
3. add vertices on the map;
4. use **Undo last**, **Finish** or **Cancel**.

The number of points is limited by the interface.

## 5.4 Duration / deadline

Non-safety spatial objects can receive a duration between **5 and 360 minutes**, in 5-minute increments.

---

# 6. Create a report

1. Long-press the map.
2. Choose **Report**.
3. Select the type.
4. Optionally enter a name and description.
5. Choose the geometry and duration.
6. Press **Publish**.

## Available report types

- Danger
- Obstacle
- Blocked route
- Impassable passage
- Open passage
- Opponent observed
- Group observed
- Movement observed
- Equipment problem
- Custom

Depending on your role, a report can be published within the team or at group level.

Scouts and managers with the required permissions can notably confirm, dispute, resolve or promote certain reports.

---

# 7. Create an objective

1. Long-press the map.
2. Choose **Objective**.
3. Enter **Objective to complete**.
4. Choose the type.
5. Choose the priority.
6. Select the geometry.
7. Set the deadline.
8. Press **Publish**.

## Objective types

- Reach a point
- Hold an area
- Capture an area
- Retrieve an object
- Join a meeting point
- Observe an area
- Custom

## Team objective or final group objective

When the role and context allow it, the form lets you choose:

- **Entire group — final objective**;
- **This team — team objective**.

The final objective is visible to group members and teams according to the Core authorization rules.

## Priorities

The interface offers:

- P0 — Urgent
- P1 — High
- P2 — Normal
- P3 — Low

---

# 8. Create an order

1. Long-press the map.
2. Choose **Order**.
3. Enter a custom instruction if necessary.
4. Choose the order type.
5. Choose the priority.
6. You can link the order to an existing **objective**.
7. You can link the order to an existing **meeting point**.
8. If necessary, LETCOOR allows you to directly create an objective or meeting point at the same location and then return to the order.
9. Choose the geometry and duration.
10. Press **Publish**.

## Order types

- Move
- Regroup
- Hold position
- Advance
- Fall back
- Defend
- Observe
- Secure an objective
- Custom

## Group leader order

When the publication is a group command order, the group leader chooses the **recipient teams**. The operational code provides that this type of order is intended for the leaders of the selected teams.

## Team order

A team leader can create orders within their team. A team order can also be linked to a parent command order when that relationship is available.

---

# 9. Create a rally point

1. Long-press the map.
2. Choose **Rally point**.
3. Give it a short name.
4. Choose a **Point** or **Circular area**.
5. Set the duration / deadline.
6. Publish.

The rally point creates a meeting point that can also be used as a reference by an order.

---

# 10. Send a safety alert

A safety alert is a priority publication.

1. Long-press the map.
2. Choose **Safety alert**.
3. Enter a message if necessary.
4. Choose the type.
5. Press **Send alert**.

## Available types

- Injury
- Stop activity
- Danger
- Missing person
- Other emergency

A custom alert requires a message.

LETCOOR reminds users in the interface that the P0 alert must be used in case of danger or need for assistance.

Depending on permissions, a manager can then **Mark as resolved**.

---

# 11. Interact with an already published object

Tap an object on the map to open its details.

Available actions depend on the object type and your permissions.

## Report

Possible actions:

- Confirm
- Dispute
- Resolve
- Extend by 15 min
- Cancel the report
- Promote to the group, when the report comes from a team and the role allows it

For certain operational objects, LETCOOR may also offer:

- **Confirm in the field**;
- **Vote to resolve**;
- **Report passage open**;
- **Remove information**.

## Objective

A user with the corresponding permission can change its status:

- In progress
- Completed
- Failed
- Cancelled

## Order

Responses may be offered depending on the order type:

- Received
- Accepted
- Completed
- Impossible

The simplified **Operations > Orders** panel uses at least the **Received** acknowledgement when the order requires a response.

## Safety alert

An authorized manager can choose **Mark as resolved**.

---

# 12. The “Command and activity” panel

The **Command** button at the top of the screen opens a separate panel for operations that are not necessarily linked to a point on the map.

It contains up to three tabs:

- **Notifications**
- **Publish**
- **History**

Tabs appear only when they contain content or when an action is authorized.

## 12.1 Notifications

Displays accessible operational objects:

- command order;
- team order;
- objective;
- final group objective;
- announcement;
- report to verify;
- verified report.

Each card may indicate:

- text;
- type;
- status;
- team/group;
- linked objective or meeting point;
- targeted teams;
- acknowledgements;
- votes;
- progress by team.

Depending on your role, buttons may offer:

- Received;
- Verify in the field;
- Remove;
- Mark as read;
- Declare completed;
- Vote completed;
- Vote impossible;
- Vote resolved;
- Resolve.

## 12.2 Publish

LETCOOR displays only publications authorized for your role and context.

The internal types currently managed by the interface include:

- Command order
- Team order
- Team objective
- Final group objective
- Announcement
- Report to verify
- Verified report

For a command order, choose the recipient teams.

For a team order, you can select a parent command order.

Then enter the description and press **Publish**.

Publications created from this panel currently use a default operational duration of about 30 minutes in the interface code.

## 12.3 History

Displays recorded events with their date, summary and object identifier.

---

# 13. The group or team menu

Tap the context name at the top left.

## Context tab

Displays:

- the **Group or team** selector;
- the number of members;
- the number of connected devices;
- session status;
- your roles;
- System / Light / Dark theme;
- language;
- your **Personal No.**, which can be copied.

The languages currently exposed by the interface are: **System, Français, English, العربية, Deutsch and Русский**. The interface automatically switches to right-to-left direction for Arabic.

## Teams tab

See [Teams](#14-teams).

## Participants tab

See [Participants and roles](#15-participants-and-roles).

## Invite tab

See [Invite a new participant](#16-invite-a-new-participant).

## Operations tab

See [Operations](#17-operations).

## Management tab

See [Group and team management](#21-group-and-team-management).

## Settings tab

Currently contains:

- offline maps;
- Bluetooth/Wi‑Fi Direct permission management;
- camera permission;
- location check.

---

# 14. Teams

The **Teams** tab displays the teams in the group.

For each team, LETCOOR notably shows:

- name;
- number of members;
- team leader;
- participant list;
- your access status for the team.

## Access statuses

- **You are a member · access ready**
- **Membership registered · receiving keys**
- **You are not part of this team**

If you are a member and access is ready, press **Open my team**.

## 14.1 Create a team

This function appears for the group leader with the corresponding permission.

1. Enter the **Team name**.
2. Choose the **Team leader** from the group members.
3. Optionally select the initial members.
4. You can use:
   - Select all;
   - 10 people;
   - 15 people;
   - Deselect all.
5. Press **Create team and appoint its leader**.

A team accepts a maximum of 200 initial members in the form, including the leader.

Selected members leave any previous team they may belong to in the same group to join the new one.

When the group already has ten or more teams, the code enforces additional minimum-size rules: active teams must have at least four members to continue expanding.

## 14.2 Replace the team leader

If the action is authorized:

1. open the team;
2. use **Replace team leader**;
3. choose a group member.

## 14.3 Validation thresholds

Authorized managers can configure:

- scout votes required to complete;
- scout votes required to declare impossible;
- votes required to resolve a report.

---

# 15. Participants and roles

The **Participants** tab displays the members of the selected context.

You can search for a participant by Personal No. or identifier.

Tap a participant to open the available actions.

## 15.1 Permanent roles and session roles

When a session is available, the manager can choose:

- **Permanent**;
- **Session**.

A permanent role remains attached to the member according to the group/team rules.

A session role applies to the selected session.

## 15.2 Assign or remove a role

Roles that you can assign appear as buttons.

An active button indicates that the role is already present. Pressing it lets you remove the role when you have the authority to do so.

There is also an **Manage a role in a team** section where you can choose:

1. the target team;
2. the role;
3. **Assign team role** or **Remove team role**.

## 15.3 Session assignment

A session administrator can set the participant to:

- Active;
- Paused;
- Left;
- Removed.

They can also choose their session team or **No team**.

Press **Apply assignment**.

## 15.4 Remove a member

When the permission is available, the **Remove from this group or team** button appears.

## 15.5 Transfer group administration

The authorized manager can select another participant and then use **Transfer administration**.

The recipient must then accept the transfer from the **Management** section.

## 15.6 Ban a device

The **Moderation** section allows, when your role permits:

- **Ban this device**;
- display banned devices;
- **Lift ban**.

A banned device continues to be rejected during new invitations until the ban is lifted.

---

# 16. Invite a new participant

Open **Invite**.

## 16.1 Choose the destination

Depending on your role, the **Destination** menu lets you choose:

- the group;
- a team.

A group administrator may have several destinations in the menu.

## 16.2 Admissions open / closed

The interface may indicate:

- **Admissions open**;
- **Admissions closed**.

If your role allows it:

- **Open access**;
- **Close access**.

A team can also inherit the group's overall closure.

## 16.3 Share the invitation

LETCOOR allows:

- link;
- QR;
- copy;
- system sharing;
- `.letcoor` file on platforms where the button is available.

## 16.4 Receive the response

After the other device imports the invitation:

1. open **Receive response**;
2. scan or paste the response link;
3. LETCOOR starts the connection.

If Internet and proximity attempts time out, the **Retry** button lets you start again.

## 16.5 Reset an invitation

The reset button invalidates/regenerates the current exchange when your role allows it.

---

# 17. Operations

The **Operations** tab lets you choose a group or team and then displays several sub-tabs depending on permissions and content:

- **Orders**
- **Announcements**
- **Roles**
- **Sharing between teams**
- **Sessions**
- **History**

## 17.1 Orders

Displays active orders with:

- type;
- priority;
- text;
- response status.

When an acknowledgement is required, the **Received** button lets you acknowledge receipt from this view.

## 17.2 Announcements

Displays active announcements.

Each announcement may include:

- type;
- text;
- pinned status;
- **Acknowledge receipt** button.

An authorized member can create an announcement by choosing:

### Types

- Information
- Important
- Group information
- Session information
- Activity rule
- Coordination

### Expiration

- 15 min
- 1 h
- 4 h
- 24 h
- No expiration

A checkbox allows you to **Pin announcement**.

---

# 18. Role campaigns

Role campaigns make it possible to temporarily open positions for a given role.

They are located in:

**Group/team menu > Operations > Roles**

## 18.1 Join a campaign

An open campaign displays:

- the role;
- its status;
- the mode;
- the number of positions already assigned / capacity.

Press **Join** to request the role.

## 18.2 Campaign modes

### First valid requests — `FIRST_VALID`

The first eligible requests are assigned automatically until the available capacity is reached.

The code allows this mode only for roles considered non-privileged.

### Approval by a manager — `ADMIN_APPROVAL`

Requests remain pending until approved by a manager.

The manager sees **Pending requests** and can press **Approve** for each participant.

## 18.3 Create a campaign

If your role allows campaign management:

1. choose the **Role**;
2. choose the **Mode** offered for that role;
3. choose the number of **Positions** from 1 to 64;
4. choose the **Duration**:
   - 15 min;
   - 1 h;
   - 4 h;
   - 24 h;
5. press **Open a campaign**.

## 18.4 Close a campaign

An authorized manager can press **Close**.

## 18.5 Withdraw your request

In **History**, a request still pending may display **Withdraw my request**.

## 18.6 Roles available for campaigns

Depending on the context and your permissions, the code exposes the following roles to campaigns:

- Group scout;
- Team scout;
- Relay;
- Cover;
- Assault.

The Group Leader role is never assigned through a campaign.

---

# 19. Sessions

A session represents a limited operational period within the group.

## 19.1 Create a session

From **Management**, if you have permission:

1. open the **Session** section;
2. enter the duration in minutes;
3. the maximum displayed duration is **56 days**;
4. press **Create a session**.

## 19.2 View sessions

In **Operations > Sessions**, LETCOOR displays:

- creation date;
- status: open/ended or assignment status;
- your team, if any;
- planned end time.

## 19.3 Manage a session

The authorized manager can:

- add **+ 1 h**;
- **End** the session.

## 19.4 Roles and assignments during a session

In **Participants**, you can choose an administered session, assign roles limited to that session and assign participants to a team/status.

---

# 20. Data sharing between teams

This function is available from a **team** in:

**Operations > Sharing between teams**

It does not automatically grant access to another team's private content. It uses a sharing offer that is explicitly created and accepted.

## 20.1 Offer sharing

1. Choose the **Target team**.
2. Choose the **Shared data**.
3. Choose the precision.
4. Set the frequency.
5. Set the expiration.
6. Press **Offer sharing**.

## 20.2 Available data classes

- General team presence
- Signal
- Team status
- Precise position
- Movement history

## 20.3 Precision

- Overview / aggregated
- Approximate
- Precise

If **Precise position** is selected, precision necessarily becomes precise in the interface.

## 20.4 Frequency

Adjustable between **5 and 300 seconds**, in 5-second increments.

## 20.5 Expiration

- 15 min
- 1 h
- 4 h
- 24 h

## 20.6 Accept or revoke

The authorized recipient team can press **Accept**.

An offer or sharing arrangement can be **Revoked** by the side with the corresponding permission.

---

# 21. Group and team management

The **Management** tab centralizes administrative functions.

## 21.1 Select a space

The **Group or team** selector lets you choose the space to administer.

## 21.2 Join an existing team

When the action is authorized, a team may offer:

- **Join**;
- **Recover access** when membership exists but keys need to be retrieved.

## 21.3 Leave a team

Press **Leave team** and then review the summary before confirming.

## 21.4 Dissolve a team

An authorized manager sees **Dissolve team**.

The confirmation states that:

- the team will be dissolved for its members;
- members remain in the group;
- other devices apply the dissolution when they receive it.

## 21.5 Leave a group

A regular member can prepare a departure plan and then confirm it.

If the participant leads teams, LETCOOR may need to dissolve those teams before departure according to the plan calculated by the Core.

## 21.6 Dissolve a group

The authorized group leader can use **Dissolve group**.

The confirmation warns that the group and its teams will be dissolved. Offline devices will have to reconnect to receive the dissolution.

## 21.7 Join a new group or team

The **Management** page also contains a **Join a group or team** block with the same invitation system as onboarding.

## 21.8 Pending invitations

When the Core exposes invitations to accept, they appear with an **Accept** button until expiration.

## 21.9 Team status

The authorized manager can publish:

- Ready
- Moving
- In position
- Rallying
- Need help
- Disconnected

## 21.10 Exact position policy

Within a team, an authorized manager can choose:

- **Allow**;
- **Deny**

for the team's exact-position policy.

## 21.11 Administration transfer

If an administration transfer is pending for you, the section displays **Accept administration transfer**.

---

# 22. Publication limits

In **Management**, authorized managers can configure publication limits for the group or team.

Limits can be defined:

- by default;
- for a specific member.

Currently exposed parameters:

- number of active safety alerts;
- reports per minute;
- reports per 4 minutes.

Form values range from 1 to 1000.

---

# 23. Location

The **Location** icon appears on the map when the platform provides native location services.

## 23.1 Enable sharing

1. Open **Location**.
2. Select **Share my location**.
3. Set the precision.

LETCOOR republishes presence periodically while sharing is active and the application can obtain the position.

## 23.2 Precision

The slider ranges from **0 m to 1 km**.

- **0 m**: precision available on the device, without any offset added by LETCOOR.
- higher value: the shared position is randomly offset within the selected radius.

## 23.3 Stop sharing

Select **Do not share my location**.

Sharing is also stopped when the context changes or when the application interrupts presence according to its lifecycle.

## 23.4 Displayed statuses

- Getting location…
- Sharing active with your group
- Sharing waiting to resume
- Location not shared

> Location sharing is not required to join a group, use the map, send orders or use the mesh.

---

# 24. Notifications

Tap the **bell** at the top of the screen.

The notification center gathers:

- group events;
- connection/transport changes;
- LETCOOR system notices.

The badge indicates the number of unread notifications.

## 24.1 Reading

Notifications are marked as read when they become sufficiently visible in the list or when the corresponding section is viewed.

## 24.2 Navigation

Tapping a notification can open:

- the Participants section;
- Teams;
- Operations;
- a map object;
- the Command panel.

## 24.3 System notifications

Bell settings let you enable/disable native system notifications when the platform supports them.

---

# 25. Offline maps

Open:

**Group/team menu > Settings > Offline maps**

## 25.1 Select an area

1. Press **Select tiles on the map**.
2. LETCOOR closes the panel and displays a grid on the map.
3. Tap the cells to keep.
4. The counter indicates the number of selected cells out of a maximum of 20.
5. Press **Confirm** to return to settings or **Cancel**.

## 25.2 Detail level

The **Detail** menu lets you select a zoom level from 3 to 14.

An area that is too large at a high detail level may be refused. The interface then asks you to reduce the detail or choose smaller cells.

## 25.3 Install

Once the cells have been selected:

1. press **Install selected cells**;
2. follow the progress;
3. you can **Cancel download**.

## 25.4 Delete a map

Installed maps are listed with their zoom and size. Press **Delete** to free up space.

---

# 26. Network connection and offline operation

LETCOOR can use several transports for the same logical network.

The interface notably recognizes:

- **Direct Internet**;
- **Internet via relay**;
- **Local network (LAN)**;
- **Local Wi‑Fi**;
- **Wi‑Fi Direct**;
- **Bluetooth**.

## 26.1 Logical mesh

LETCOOR does not require every member to be directly connected to every other member.

Example:

```text
Phone A ↔ Phone B ↔ Phone C ↔ Phone D
```

An authorized event can be relayed between peers according to the topology and the group/team scope rules.

The physical transport and LETCOOR identity are separate: a peer remains identified by its LETCOOR identity even if the network path changes.

## 26.2 Without Internet

To maximize the chances of operating without Internet:

- enable Wi‑Fi;
- enable Bluetooth;
- allow nearby devices;
- allow the local network if Android asks for it;
- accept system visibility/pairing when LETCOOR requests it;
- keep LETCOOR in the foreground during the first connection;
- bring the devices closer together during initial bootstrap;
- do not refuse system dialogs required for proximity radio.

## 26.3 Proximity transport status

LETCOOR can display separately:

- Local Wi‑Fi;
- Wi‑Fi Direct;
- Bluetooth;

with statuses such as:

- permission required;
- activation required;
- initializing;
- ready;
- searching;
- peer found;
- connecting;
- group formed;
- LETCOOR authentication;
- connected;
- recovery;
- unavailable.

## 26.4 Wi‑Fi Direct busy

If Android indicates that Wi‑Fi Direct is busy, LETCOOR may attempt recovery. The Wi‑Fi Direct information screen notably recommends checking:

- that Wi‑Fi is enabled;
- that tethering/hotspot does not conflict with Wi‑Fi Direct;
- that another Wi‑Fi Direct discovery/connection is not already in progress.

## 26.5 The network can change transport

The status at the top of the screen may display different transports during the session. LETCOOR may have alternative routes to a peer and use the available route according to network conditions.

---

# 27. Privacy, locking and recovery

LETCOOR applies several protective behaviors when private group data can no longer be verified with other members.

## 27.1 Lock after absence

The interface code includes a screen:

**Session locked after one minute of absence.**

Press **Reconnect** to regain access.

## 27.2 Verifying connection to members

When privacy recovery is required, LETCOOR displays:

**Verifying connection to members…**

It attempts to find a reachable member and may display details of proximity transports.

## 27.3 Automatic local deletion

For certain groups configured with automatic recovery, if reconnection is not possible within the expected period, the group's local data may be deleted **after verification**.

The current interface announces a twenty-minute deadline for affected groups.

When offered, you can:

- delete/reset local data;
- or choose **Keep data at my own risk**, which disables automatic deletion for this context.

LETCOOR warns that keeping this data may increase the risk in the event of physical compromise of the device.

## 27.4 Desktop protection

On desktop, the private view can be hidden/blurred when the window loses focus and then refreshed before being displayed again.

---

# 28. Available roles

The LETCOOR domain model defines nine roles.

| Role | General function in the current code |
|---|---|
| **Group administrator** (`GROUP_ADMIN`) | Group administration, team and session creation, member/role management, campaigns, dissolution, administration transfer, announcements. |
| **Group coordinator** (`GROUP_LEADER`) | Group-level coordination, group orders/objectives/reports, campaigns and announcements according to permissions. |
| **Team leader** (`TEAM_LEADER`) | Orders/objectives/meeting points/status for their team, inter-team sharing, announcements, team campaigns. |
| **Group scout** (`GROUP_SCOUT`) | Reporting and confirmation/promotion at group level according to permissions. |
| **Team scout** (`TEAM_SCOUT`) | Team report/reporting, confirmation and promotion according to permissions. |
| **Relay** (`TRANSMITTER`) | Relay capability provided by the domain and publication of certain summarized presence data according to policy; this role does not grant access to other teams' private data. |
| **Cover** (`COVER`) | Operational label with the member's basic capabilities. |
| **Assault** (`ATTACKER`) | Operational label with the member's basic capabilities. |
| **Member** (`MEMBER`) | Basic capabilities: normal reporting within their team when permitted, safety alert, order response, authorized presence and participation in campaigns. |

> Permissions are calculated by the Core and are additive. The interface only displays actions that are actually authorized. Belonging to a group does not automatically grant access to the private data of all its teams.

---

# 29. Preparation tips before an activity

For real-world use, especially in an area where Internet access may be poor:

1. Install the same version of LETCOOR on all devices.
2. Create the group before the activity begins.
3. Have participants join while they are still physically close.
4. Accept proximity permissions on each Android device.
5. Enable Bluetooth and Wi‑Fi.
6. Test at least one connection without mobile data if offline operation is important.
7. Create teams and assign leaders before dispersing.
8. Open a session if you want session-specific roles/assignments and the corresponding history.
9. Download the required offline maps before losing Internet access.
10. Check that participants know how to open:
    - Notifications;
    - Command;
    - their team;
    - the Safety alert function.
11. Enable location sharing only if you genuinely want to publish it.

---

# 30. Troubleshooting

## The two devices cannot see each other offline

Check on both devices:

- Wi‑Fi enabled;
- Bluetooth enabled;
- **Nearby devices** permissions granted;
- local network permission granted if Android requests it;
- app visible/discoverable if the system asks for confirmation;
- LETCOOR in the foreground during initial discovery.

If Android opens location settings, enable location services to maximize discovery compatibility. This does not enable LETCOOR location sharing.

## “Wi‑Fi Direct unavailable” or “busy”

- temporarily disable any manual tethering/hotspot;
- wait a few seconds;
- restart the attempt;
- check that another application or Wi‑Fi Direct connection is not active.

## The QR code does not work

- wait until all parts of the QR code have been read;
- bring the screens closer together;
- increase the brightness of the screen displaying the QR code;
- use the camera zoom slider;
- use the link instead of the QR code if necessary.

## Camera access is denied

- use the link;
- or open the Windows/Android camera settings from LETCOOR when the button is offered.

## The link is accepted but the connection times out

- check Internet or proximity;
- bring the devices closer together;
- enable Wi‑Fi and Bluetooth;
- accept system dialogs;
- press **Retry** when the button appears.

## I am in the group but not in a team

Open:

**Context > Teams** or **Management**.

If the team allows joining, use **Join**. A team invitation may also directly admit the participant to the parent group and the targeted team according to the received ticket.

## “Membership registered · receiving keys”

The membership is known, but cryptographic access to the team is not yet ready. Keep the devices connected to allow the keys to be retrieved/synchronized. If the **Recover access** button appears in Management, use it.

## An object is not visible

Check:

- the selected group/team;
- your permissions;
- the object's expiration;
- network synchronization;
- that a private team object is not automatically visible to other teams.

## Location is not displayed

- check the location permission;
- check that **Share my location** is selected;
- check the current group;
- wait for the next periodic publication;
- check that the team policy allows the required precision.

---

# 31. Quick summary

## To join LETCOOR

```text
Inviter
  ↓
Invite
  ↓
QR or link
  ↓
Invited device imports
  ↓
Invited device produces a response
  ↓
Inviter scans/pastes the response
  ↓
Connection + authentication + admission
```

## To create something on the map

```text
Long-press the map
  ↓
Report / Objective / Order / Rally point / Safety alert
  ↓
Fill in the form
  ↓
Choose area / duration if available
  ↓
Publish
```

## To manage a group

```text
Group name at top left
  ↓
Context | Teams | Participants | Invite | Operations | Management | Settings
```

## For a role campaign

```text
Operations
  ↓
Roles
  ↓
Choose role + mode + positions + duration
  ↓
Open a campaign
  ↓
Members join
  ↓
Automatic assignment or manager approval depending on the mode
```

## To operate without Internet

```text
Wi‑Fi ON
Bluetooth ON
Proximity permissions allowed
Local network allowed if requested
Pairing/visibility accepted if requested
Devices close together on first contact
LETCOOR open in the foreground
```

LETCOOR can then use the available transports and relay authorized information between peers according to the mesh topology.

---

**LETCOOR 1.0.0 — User Documentation**
