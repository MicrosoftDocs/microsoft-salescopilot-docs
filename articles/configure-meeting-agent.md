---
title: Configure recordings and notifications for sales meetings
description: Learn how to configure auto recording and notifications for sales meetings to ensure sellers are well-prepared and important details are captured.
ms.date: 07/03/2025
ms.topic: how-to
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
ai-usage: ai-assisted
---

# Configure recordings and notifications for sales meetings

As an administrator, you can optimize the meeting experience for your sellers by enabling or disabling auto recording for all sales meetings and configuring the time of pre-meeting notifications. Pre-meeting notifications are sent to sellers before their meetings to help them prepare. You can choose if a daliy summary of meetings should be sent to sellers or if they should receive notifications before each meeting or both. These features help ensure that sellers are well-prepared and that important meeting details are captured seamlessly.

## Enable or disable auto recording for sales meetings

Auto recording enables your sellers to automatically record all sales meetings with external contacts without having to remember to start the recording manually. By default, the feature is turned off.

Auto recording is applicable only to sales meetings that have the [**Copilot for Sales** app added automatically](create-teams-meeting.md#add-the-copilot-for-sales-app-automatically-to-a-teams-meeting) before the meeting. 

> [!NOTE]
> If a meeting is marked as private, it isn't recorded. 

To turn on auto recording for sales meetings:

1. In Copilot for Sales admin settings, select **Meeting agent**.
2. Under **Recordings**, select **Auto-record sales meetings**.
3. In the **Auto-record sales meetings** pane, select **On**.
4. Select **Save**.

If you want to turn off auto recording for sales meetings, follow the same steps and select **Off** in step 3.

## Configure daily summary of meetings

The daily summary of meetings helps sellers stay organized by providing a single notification summarizing the next five upcoming sales meetings. It reduces notification fatigue while delivering critical insights. The notification categorizes meetings by date, includes clickable meeting titles, and provides essential details like duration and agenda summaries. By default, the feature is turned off. 

To turn on the daily summary of meetings feature:

1. In Copilot for Sales admin settings, select **Meeting agent**.
2. Under **Notifications**, select **Daily digest**.
3. In the **Daily digest** pane, select **On**.
4. From the **Delivery time** list, select the time when the daily digest is sent. By default, 7:30 AM is selected.
5. Select **Save**.

If you want to turn off the daily summary of meetings feature, follow the same steps and select **Off** in step 3.

## Configure pre-meeting preparation notifications

[Pre-meeting preparation notifications](meeting-prep.md) are sent to sellers before each meeting to help them prepare. By default, pre-meeting preparation notifications are sent one hour before the meeting. You can change the time based on your organizational needs.

To configure the time of pre-meeting preparation notifications:

1. In Copilot for Sales admin settings, select **Meeting agent**.
2. Under **Notifications**, select **Pre-meeting preparation**.
3. In the **Pre-meeting preparation** pane, select **On** or **Off** to enable or disable the feature.
4. From the **Delivery interval** list, select the time interval before the meeting when the notification is sent. By default, 1 hour is selected.
5. Select **Save**.

### Related information

- [Create a Teams meeting](create-teams-meeting.md)
- [Generate a meeting summary](generate-meeting-summary.md)
- [Meeting preparation card](meeting-prep.md)