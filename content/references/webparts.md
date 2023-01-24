+++
title = "Webparts"
+++

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Web Parts](#web-parts)
  - [Combined Search Web Part](#combined-search-web-part)
- [Edit Widget Explanations](#edit-widget-explanations)
  - [Search Query](#search-query)
    - [Examples](#examples)
    - [Debugging Queries](#debugging-queries)
    - [Tips](#tips)
    - [Avoid Nesting Folders in SharePoint Sites](#avoid-nesting-folders-in-sharepoint-sites)
    - [Form View](#form-view)
  - [Row limit](#row-limit)

## Web Parts

### Combined Search Web Part

&emsp; This webpart can display multiple query results through the use of tabs.

**Example**

Example Recipe: [Combined Search Videos](/recipes/webparts/#combined_search_videos)

![combined-search-videos.png](https://i.postimg.cc/WbRtkTHF/combined-search-videos.png)

## Edit Widget Explanations

### Search Query

&emsp; In Powell, you may have seen this Search query box, called either *Search query* or *Search query template*:

![search query](https://i.postimg.cc/xC8js7F2/search-query.png)

The language used in this particular search box is [Keyword Query Language (KQL)](https://learn.microsoft.com/en-us/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference). KQL is used to build search queries for the SharePoint search service. For syntax and more, please refer to documentation [here](https://learn.microsoft.com/en-us/sharepoint/dev/general-development/building-search-queries-in-sharepoint). These search queries allow developers to query the SharePoint site, often times for looking for info in site contents.

Keep in mind that there is an entirely separate query language with the same acronym that Microsoft uses for Azure called Kusto Query Language (KQL). This is *not* used in SharePoint.

#### Examples

&emsp; Query for mp4 videos in the entire site contents:

Search query template
```
FileType: mp4
```
KQL filter = `FileType: mp4`


&emsp; Query for mp4 Videos in the Communications Document Library:

Search query template
```
PATH: "https://unifiedphysicianmgt.sharepoint.com/sites/UnifiedWomensHealth/Communications/Forms" FileType: mp4
```
- SharePoint base URL = `https://unifiedphysicianmgt.sharepoint.com/sites/UnifiedWomensHealth`
- SharePoint Document Library = `/Communications`
- SharePoint Document Library View = `/Forms`
- Additional KQL filter = `FileType: mp4`

#### Debugging Queries

&emsp; The most efficient method of debugging KQL queries in Powell SharePoint is to use the *Test* button on the Query Builder.
1. On your SharePoint Site with Powell, click on *Edit* in the top right corner.
2. *Edit* the webpart that you wish to debug. If it's combined search webpart, you might need to click on an internal edit button as well.
3. Under *Content Search edit mode*, expand Query Builder
4. The *Test* button is at the bottom just before the *Display* header.

When you're done testing, always *Discard changes* in the upper left corner. Otherwise, there is a timer that will take you out of edit mode involuntarily.

#### Tips

#### Avoid Nesting Folders in SharePoint Sites

&emsp; Folders as seen on the *site contents* level in the SharePoint site are special folders called *Document Library* folders. If we want to limit grabbing items from a specific folder can only limit the scope of information grabbed by Document Library folders. The same information will be grabbed at the Document Library level folder will be grabbed from the nested folder. Nested folders do not help with organization. Only keep files and lists folders for content in Powell. Do not use folders within folders.

#### Form View

&emsp; You may be tempted to use:

`PATH: "https://unifiedphysicianmgt.sharepoint.com/sites/UnifiedWomensHealth/Communications"`

but we actually need to use

`PATH: "https://unifiedphysicianmgt.sharepoint.com/sites/UnifiedWomensHealth/Communications/Forms"`

because we need the Forms view of the files.

### Row limit
&emsp; Think of a SharePoint list. Each row in this case is an item on the list. Therefore, row limit really means item limit.

**Example**

&emsp; In the [grid list of links recipe](/recipes/webparts/#grid-list-of-links), we want an arbitrary max of 27 rows or 27 items that will be grabbed from the SharePoint List
