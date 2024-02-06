---
title: Dataverse tables used in the Copilot for Sales dashboard reports
description: Dataverse tables used in Copilot for Sales dashboard reports. Includes tables for conversation data, transcripts, tags, insights, and more.
ms.date: 02/01/2024
ms.topic: article
ms.service: microsoft-sales-copilot
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.custom:
  - ai-gen-docs-bap
  - ai-gen-desc
  - ai-seo-date:01/28/2024
---

# Dataverse tables used in the Copilot for Sales dashboard reports (preview)

[!INCLUDE [preview-note](includes/preview-note.md)]

[!INCLUDE [preview-banner](includes/preview-banner.md)]

The following table lists the Dataverse tables used in the dashboard reports.


| Table | Where in dashboard? | Use  |
|----------------------------------|--------------------------------------------|------------------------------------------|
| SCI Conversation                 | Time filter                                | The minimum and maximum values of the time filter are set according to the Start time field of the table.                |
| SCI Conversation                 | Team or Seller filters                     | The Team or Seller filters filter the data in the dashboard based on the owner of the table.                             |
| SCI Conversation                 | Activity type filter                       | Displays the source for the type of activity (for example, email, phone call, or meeting).                               |
| SCI Conversation                 | Coaching opportunities and call recordings | Displays the count of daily conversations by conversation type.                                                                          |
| SCI Conversation                 | Call recordings                            | Displays type, time, subject, and owner of the conversation in a table.                                                  |
| Transcript                       | Call recordings                            | Displays the transcript on each conversation's summary page.                                                             |
| Conversation Comment             | Call recordings                            | Displays the comments on transcript on each conversation's summary page.                                                 |
| Recording                        | Call recordings                            | Displays the recording on each conversation's summary page.                                                              |
| Tag                              | Tags filter                                | Allows you to filter data on the dashboard based on the tags.                                                            |
| Tag                              | Call recordings                            | Displays tags in the **Tags** column.                                                                                    |
| System tag                       | Call category filter                       | Allows you to filter data on the dashboard based on the call category.                                                   |
| System tag                       | Call recordings                            | Displays system tags on the user interface.                                                                              |
| Aggregated insights              | Coaching opportunities                     | Displays data for Switches per call and Longest customer monologue KPIs.                                                 |
| Aggregated insights              | Coaching opportunities and Call recordings | Displays count of daily recorded hours by conversation type.                                                             |
| General customer sentiment       | Customer insights                          | Displays the customer sentiment score.                                                                                   |
| General customer sentiment       | Call recordings                            | Displays the customer sentiment in the call recordings table.                                                            |
| Conversation subjects            | Call recordings                            | Displays conversation segments over the playback timeline on the conversation summary page.                              |
| Participants insights            | Coaching opportunities                     | Displays data for Pause before speak, Longest seller monologue, Switches per call, and Talk to listen ratio KPIs         |
| Participants insights            | Call recordings                            | Displays the participants data on the conversation summary page.                                                         |
| Participant's sentiment          | Call recordings                            | Displays the participant's sentiment on the playback timeline on the conversation summary page.                          |
| Tracked keywords and competitors | Call recordings                            | Displays the tracked keywords and competitors in the transcript and Highlights section on the conversation summary page. |
| Segment sentiment                | Call recordings                            | Indicates the sentiment of specific utterances on the conversation summary page.                                         |
| Summary suggestion               | Call recordings                            | Displays the summary suggestion on the conversation summary page.                                                        |
| Questions                        | Coaching opportunities                     | Displays data for the Engaging questions rate KPI.                                                                       |
| Questions                        | Call recordings                            | Displays questions on the conversation summary page.                                                                     |
| Action items                     | Call recordings                            | Displays action items on the conversation summary page.                                                                  |

