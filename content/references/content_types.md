+++
title = "Content Types"
weight = 1
+++

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Content Types](#content-types)
  - [Standard Content Types](#standard-content-types)
  - [Partners Content Types](#partners-content-types)
  - [Custom Content Types](#custom-content-types)
- [Standard Content Types Reference](#standard-content-types-reference)
  - [Announcement](#announcement)
  - [Comment](#comment)
  - [Contact](#contact)
  - [East Asia Contact](#east-asia-contact)
  - [Event](#event)
  - [Issue](#issue)
  - [Item](#item)
  - [Link](#link)
  - [Message](#message)
  - [Post](#post)
  - [Reservations](#reservations)
  - [Schedule and Reservations](#schedule-and-reservations)
  - [Schedule](#schedule)
  - [Task](#task)
  - [Workflow Task (SharePoint 2013)](#workflow-task-sharepoint-2013)


<table>
    <caption>A custom <i>Content Type</i> is composed of a standard <i>Content Type</i> plus a custom <i>Type</i></caption>
    <thead>
        <tr>
            <th>Layer 1</th>
            <th>Layer 2</th>
            <th>Layer 3</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=4>custom <i>Content Type</i></td>
            <td rowspan=2>standard <i>Content Type</i></td>
            <td><i>Type</i></td>
        </tr>
        <tr>
            <td><i>Type</i></td>
        </tr>
        <tr>
            <td rowspan=1>custom <i>Type</i></td>
        </tr>
    </tbody>
</table>

## Content Types
&emsp; A *Content Type* is the type of content allowed in a *List Template*. *List Templates* can be composed of several *Content Type*. A *Content Type* is composed of one or more *Types*. Although there are technically three types of content types according to Powell, in my experience, there are really only two kinds: standard *Content Type* and custom *Content Type*. 

### Standard Content Types
&emsp; Content types that come with Powell.

### Partners Content Types
&emsp; Custom content types that have been made by your business entity.

### Custom Content Types
&emsp; Custom content types that have been made by your SharePoint tenant.

## Standard Content Types Reference

### Announcement
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Body | Body | Note
Content Type | ContentType | Computed
Expires | Expires | DateTime
### Comment
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Body | Body | Note
Content Type | ContentType | Computed
### Contact
Display name | Internal name | Type
--- | --- | ---
Company | Company | Text
Title | Title | Text
Full Name | FullName | Text
Business Phone | WorkPhone | Text
Title | LinkTitleNoMenu | Computed
E-Mail | EMail | Text
Job Title | JobTitle | Text
ZIP/Postal Code | WorkZip | Text
Content Type | ContentType | Computed
Last name Phonetic | LastNamePhonetic | Text
City | WorkCity | Text
Country/Region | WorkCountry | Text
Company Phonetic | CompanyPhonetic | Text
Comments | Comments | Note
Address | WorkAddress | Note
First Name Phonetic | FirstNamePhonetic | Text
Title | LinkTitle | Computed
Fax Number | WorkFax | Text
Web Page | WebPage | URL
State/Province | WorkState | Text
First name | FirstName | Text
Home Phone | HomePhone | Text
Mobile Number | CellPhone | Text
### East Asia Contact
Display name | Internal name | Type
--- | --- | ---
Company | Company | Text
Title | Title | Text
Full Name | FullName | Text
Business Phone | WorkPhone | Text
Title | LinkTitleNoMenu | Computed
E-Mail | EMail | Text
Job Title | JobTitle | Text
ZIP/Postal Code | WorkZip | Text
Content Type | ContentType | Computed
Last name Phonetic | LastNamePhonetic | Text
City | WorkCity | Text
Country/Region | WorkCountry | Text
Company Phonetic | CompanyPhonetic | Text
Comments | Comments | Note
Address | WorkAddress | Note
First Name Phonetic | FirstNamePhonetic | Text
Title | LinkTitle | Computed
Fax Number | WorkFax | Text
Web Page | WebPage | URL
State/Province | WorkState | Text
First name | FirstName | Text
Home Phone | HomePhone | Text
Mobile Number | CellPhone | Text
### Event
Display name | Internal name | Type
--- | --- | ---
Event Cancelled | EventCanceled | Boolean
UID | UID | Guid
Title | Title | Text
TimeZone | TimeZone | Integer
Location | Location | Text
WorkspaceUrl | Workspace | URL
Category | Category | Choice
Recurrence | fRecurrence | Recurrence
Content Type | ContentType | Computed
Duration | Duration | Integer
Event Type | EventType | Integer
MasterSeriesItemID | MasterSeriesItemID | Integer
Comments | Comments | Note
Start Date | StartDate | DateTime
RecurrenceData | RecurrenceData | Note
XMLTZone | XMLTZone | Note
End Time | EndDate | DateTime
Workspace | WorkspaceLink | CrossProjectLink
Recurrence ID | RecurrenceID | DateTime
### Issue
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Related Issues | RelatedIssues | Lookup
Assigned To | AssignedTo | User
Priority | Priority | Choice
Category | Category | Choice
Append-Only Comments | V3Comments | Note
Content Type | ContentType | Computed
Issue ID | LinkIssueIDNoMenu | Computed
Issue Status | IssueStatus | Choice
Due Date | TaskDueDate | DateTime
### Item
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Title | LinkTitleNoMenu | Computed
Type | DocIcon | Computed
Created By | Author | User
Content Type | ContentType | Computed
Edit | Edit | Computed
Modified | Modified | DateTime
Title | LinkTitle | Computed
Created | Created | DateTime
Modified By | Editor | User
Attachments | Attachments | Attachments
### Link
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Title | LinkTitleNoMenu | Computed
Content Type | ContentType | Computed
URL | URL | URL
Comments | Comments | Note
Title | LinkTitle | Computed
URL | URLwMenu | Computed
URL | URLNoMenu | Computed
### Message
Display name | Internal name | Type
--- | --- | ---
ToggleQuotedText | ToggleQuotedText | Computed
Title | Title | Text
Threading | Threading | Computed
Posted By | PersonViewMinimal | Computed
Version | _UIVersionString | Text
Body | Body | Note
Title | LinkTitleNoMenu | Computed
Parent Item ID | ParentItemID | Integer
Shortest Thread-Index | ShortestThreadIndex | Note
Indentation | Indentation | Computed
Message ID | Message Id | Text
Quoted Text Was Expanded | QuotedTextWasExpanded | Computed
Full Body | FullBody | Computed
Content Type | ContentType | Computed
Posting Information | StatusBar | Computed
Correct Body To Show | CorrectBodyToShow | Computed
Indentation Level | IndentLevel | Computed
Threading Controls | ThreadingControls | Computed
Body Was Expanded | BodyWasExpanded | Computed
Limited Body | LimitedBody | Computed
Post | BodyAndMore | Computed
Shortest Thread-Index Id | ShortestThreadIndexId | Text
Trimmed Body | TrimmedBody | Note
More Link | MoreLink | Computed
Discussion Title | DiscussionTitleLookup | Lookup
References | Email References | Note
Modified By | My Editor | User
Less Link | LessLink | Computed
Parent Folder Id | ParentFolderId | Integer
Is Root Post | IsRootPost | Computed
Discussion Subject | DiscussionTitle | Computed
Parent Item Editor | ParentItemEditor | User
Reply | ReplyNoGif | Computed
PostedBy | PersonImage | Computed
Thread Index | ThreadIndex | ThreadIndex
E-Mail Sender | EmailSender | Note
Shortest Thread-Index Id Lookup | ShortestThreadIndexIdLookup | Lookup
### Post
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Body | Body | Note
Category | PostCategory | Lookup
Content Type | ContentType | Computed
Published | PublishedDate | DateTime
### Reservations
Display name | Internal name | Type
--- | --- | ---
Event Cancelled | EventCanceled | Boolean
UID | UID | Guid
Title | Title | Text
TimeZone | TimeZone | Integer
Location | Location | Text
WorkspaceUrl | Workspace | URL
Category | Category | Choice
Recurrence | fRecurrence | Recurrence
Content Type | ContentType | Computed
Duration | Duration | Integer
Event Type | EventType | Integer
MasterSeriesItemID | MasterSeriesItemID | Integer
Comments | Comments | Note
Start Date | StartDate | DateTime
RecurrenceData | RecurrenceData | Note
XMLTZone | XMLTZone | Note
End Time | EndDate | DateTime
All Day Event | fAllDayEvent | AllDayEvent
Workspace | WorkspaceLink | CrossProjectLink
Recurrence ID | RecurrenceID | DateTime
### Schedule and Reservations
Display name | Internal name | Type
--- | --- | ---
Event Cancelled | EventCanceled | Boolean
UID | UID | Guid
Title | Title | Text
TimeZone | TimeZone | Integer
Location | Location | Text
WorkspaceUrl | Workspace | URL
Category | Category | Choice
Recurrence | fRecurrence | Recurrence
Content Type | ContentType | Computed
Duration | Duration | Integer
Event Type | EventType | Integer
MasterSeriesItemID | MasterSeriesItemID | Integer
Comments | Comments | Note
Start Date | StartDate | DateTime
Participants | ParticipantsPicker | User
RecurrenceData | RecurrenceData | Note
XMLTZone | XMLTZone | Note
End Time | EndDate | DateTime
All Day Event | fAllDayEvent | AllDayEvent
Workspace | WorkspaceLink | CrossProjectLink
Recurrence ID | RecurrenceID | DateTime
### Schedule
Display name | Internal name | Type
--- | --- | ---
Event Cancelled | EventCanceled | Boolean
UID | UID | Guid
Title | Title | Text
TimeZone | TimeZone | Integer
Location | Location | Text
WorkspaceUrl | Workspace | URL
Category | Category | Choice
Recurrence | fRecurrence | Recurrence
Content Type | ContentType | Computed
Duration | Duration | Integer
Event Type | EventType | Integer
MasterSeriesItemID | MasterSeriesItemID | Integer
Comments | Comments | Note
Start Date | StartDate | DateTime
Participants | ParticipantsPicker | User
RecurrenceData | RecurrenceData | Note
XMLTZone | XMLTZone | Note
End Time | EndDate | DateTime
All Day Event | fAllDayEvent | AllDayEvent
Workspace | WorkspaceLink | CrossProjectLink
Recurrence ID | RecurrenceID | DateTime
### Task
Display name | Internal name | Type
--- | --- | ---
Title | Title | Text
Body | Body | Note
Assigned To | AssignedTo | User
Priority | Priority | Choice
% Complete | Percent Complete | Number
Content Type | ContentType | Computed
Start Date | StartDate | DateTime
Predecessors | Predecessors | Lookup
Due Date | TaskDueDate | DateTime
Task Status | TaskStatus | Choice
Related Items | RelatedItems | Note
### Workflow Task (SharePoint 2013)
Display name | Internal name | Type
--- | --- | ---
Instance Id | WF4InstanceId | Text
Title | Title | Text
Task Outcome | TaskOutcome | Choice
Body | Body | Note
Assigned To | AssignedTo | User
Priority | Priority | Choice
% Complete | Percent Complete | Number
Content Type | ContentType | Computed
Start Date | StartDate | DateTime
Predecessors | Predecessors | Lookup
Due Date | TaskDueDate | DateTime
Task Status | TaskStatus | Choice
Related Items | RelatedItems | Note
