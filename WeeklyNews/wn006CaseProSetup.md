# UParters - Proper use of features

How to direct message an anonymous reporter? That's the main purpose of U-Partners, where you can setup some strategies to access previous labeled messages and chat with contacts anonymously.

## Understand the scenario

To label messages correctly you need to build the flow like the example below, where the *Add Label* actionset is placed right after the *Wait for response*. That's very important as the Label feature is direct linked to the flow step.

![LabelStep](/img/WN/wn006LabelStep.png "Where to place the Add Label actionset")

It's also possible to create labels not synced and assign a contact's group to have all messages labeled.
To start creating it, go to your U-Partners workspace, select Organization (at the top bar) and hit New at the Labels tab.

![CustomLabel](/img/WN/CasePro_customLabel.png "Click new at Labels tab")

You'll have to name the label, give it a short description and select the group that will have messages labeled.

![LabelSetup](/img/WN/CasePro_setupCustomlabel.png "Fill name and descrition, select the group and save.")

## Messaging the contact

You can send a single message to the contact by clicking Reply. Contact's source message will be archived and the sent message will be received at the same channel they used to chat.

![QuickReply](/img/WN/CasePro_quickReply.png "Sending a quick reply.")

### Opening a case

If you want to chat with the contact, a case needs to be opened.

![OpenCase](/img/WN/CasePro_OpenCase.png "Open a Case to start a conversation.")

A new window will popup, asking for additional details.

![OpenCaseDetails](/img/WN/CasePro_Caseproperties.png "Add case title and assign if necessary.")

Type the message to be sent and hit send.

![SendCaseMessage](/img/WN/CasePro_SendCaseMessage.png "Start the conversation.")

### Closing a case

Once the conversation is done, you must close the case by hitting Close.

![CloseCase](/img/WN/CasePro_CloseCase.png "Finish the conversation.")

Add a final note to the case and close it.

![CloseCaseNote](/img/WN/CasePro_CloseCaseNote.png "Finish the conversation.")

> Importance of closing all cases: All messages within cases are archived. Leaving cases opened will make that contact's messages prematurely archived, and that can compromise polls accuracy.

### Preventing the chat to send messages while the contact has a case open

As you will set the **uncaught message** trigger, all contact's messages will be replied by the flow set up.
You'll have to set a group for chatting contacts and sort it at that flow. In the example I named that group **Bot**. All contacts should be added to this group, you can use a dynamic group for that.

![SortingGroups](/img/WN/CasePro_StopChat.png "Sort contact's group.")

You'll also need a flow just to add contacts back to that group, in this example a named it **Activate chat**. And then, let's set up U-Partners to work with that.

At the U-Partners properties, select *Suspend groups* and *Follow-up Flow*.

![StoppingChat](/img/WN/CasePro_StopChatOpt.png "Point the group that should be suspended, the flow that will add back to group and save.")

Now you'll be able to talk freely as long as the case remains open, and after closed the contact will experience messages replies again.