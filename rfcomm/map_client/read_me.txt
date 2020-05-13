-------------------------------------------------------------------------------
Message Access (MAP) Client app
-------------------------------------------------------------------------------

Overview
--------
The Message Access Client application is designed to connect and access
service on the Message Access Server device. It can be used to access
SMS-MMS messages or email received on the Message Access Server device such
as a smartphone.

See chip specific readme for more information about the BT SDK.

Features demonstrated
---------------------
 - MAS instance discovery
 - Connect/disconnect to MAP server
 - Get folder listing
 - Change folder
 - Get message listing
 - Get message
 - Delete/undelete message
 - Send message
 - Register to receive new message notification

Instructions
------------
To demonstrate the app, work through the following steps.
1. Plug the WICED eval board into your computer
2. Build and download the application (to the WICED board)
3. Launch Client Control application
4. From Client Control UI, Open port to connect to the eval board
5. Start BR/EDR discovery
6. Select the MAP server device to be connected
7. In MAP Client tab, click Get Services button
8. Select a service (SMS or Email) and click Connect button
9. Accept pairing request and MAP access request on the phone
10. On the Client Control UI, select a folder in the folder list (such as inbox)
   to display the list of messages in this folder
11. Click a message ID in the message list to show message content
12. Click Delete button to delete the message
13. Change to deleted folder, select the message deleted in the previous step,
   click Undelete button, verify the message goes back to the original folder
14. Change to inbox folder, select a message, click Reply button. Sender's phone
   number (email address and Subject in the case of email) will be copied over
   to the send side
15. Enter some text and click Send button, verify the message is sent
16. Send a message from another phone, UI will show a trace saying a new message
   had been received and the inbox will automatically update to show the ID of
   the new message

Note: iOS MAP behavior
----------------------
1. When you try to connect, you will see message that connection is not
   successful, though pairing is successful. Go to the Bluetooth menu and enable
   "Show Notifications " for Map_client device. After this step, you will be
   able to connect successful.
2. After first connection with MAP client, you will see only 10 messages in Inbox. You will
   not be able to see messages in other folders such as Outbox or Deleted. On switching from
   Inbox to other folder and switching back to Inbox, you will not see messages in Inbox.
   On older iOS releases, you will not be able any messages in any folders.
3. If you receive messages from another phone while you are connected to MAP client app,
   those messages will appear in Inbox.


-------------------------------------------------------------------------------
