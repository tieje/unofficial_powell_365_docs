+++
title = "Webparts"
+++

---

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Species](#species)
  - [Banner](#banner)
  - [Combined Search](#combined-search)
  - [Discussion Tiles](#discussion-tiles)
  - [Divider](#divider)
  - [Script Editor](#script-editor)
  - [Search webpart](#search-webpart)
  - [Text](#text)
    - [Text Caveats](#text-caveats)
  - [Title](#title)
- [Edit Widget Explanations](#edit-widget-explanations)
  - [Search Query](#search-query)
    - [KQL Cheat Sheet](#kql-cheat-sheet)
    - [Examples](#examples)
    - [Debugging Queries](#debugging-queries)
  - [Avoid Nesting Folders in SharePoint Sites](#avoid-nesting-folders-in-sharepoint-sites)
  - [Form View](#form-view)
  - [Row limit](#row-limit)
- [Display or Select Widgets](#display-or-select-widgets)
  - [Species](#species-1)
    - [Application Tiles 2](#application-tiles-2)
- [Tips and Tricks](#tips-and-tricks)
  - [Determine the Type of Webpart By Inspecting SharePoint Site with Dev Tools](#determine-the-type-of-webpart-by-inspecting-sharepoint-site-with-dev-tools)

---

## Species

### Banner

&emsp; It is what it says it is. Unfortunately, there are two *Title* inputs and a *Description* which gets confusing. The first *Title* is used internally for the webpart. The second *Title* is the top part of the banner with the arrow. The text below it is the description. If the text for description is not included, it defaults to the format **[Page Name] - [Title]**. If the text for the title is not included, the top text defaults to the page name.

### Combined Search

&emsp; This webpart can display multiple query results through the use of tabs.

**Example**

Example Recipe: [Combined Search Videos](/recipes/webparts/#combined_search_videos)

![combined-search-videos.png](https://i.postimg.cc/WbRtkTHF/combined-search-videos.png)

### Discussion Tiles

&emsp; This webpart can only be used by pre-programmed Powell Intranet site templates like the [Water Fountain Page](/recipes/pow_example_pages/#water-fountain-page). In other words, this webpart is useless to Powell users.
![Discussion Tiles](https://i.postimg.cc/fL24hZss/discussion-tiles.png)

### Divider

&emsp; This webpart is basically the equivalent of `<hr>` html tag.

&emsp; Example [recipe](/recipes/webparts/#title-text-statement)

### Script Editor

&emsp; This webpart allows users to insert a script tag from Powell Manager.

![Script Editor](https://i.postimg.cc/RF8pHtM0/script-editor.png)

### Search webpart

&emsp; Powell support once told me in a call that "about 80% of the webparts that we use are *Search* webparts". That being said, a picture of a *Search* webpart is not enough to show what it is or what it can do. It's fairly moldable to the user's desires as it can be used with most Display widgets.

### Text

&emsp; The very last option that looks like `< >` shows what is going be on the page in raw HTML. Unfortunately, you'll need to save, sync, and then look at the SharePoint site to look at your pages. There is a bug where deleting empty spacer tags like below while in code view and then save, the empty tags will still remain there. Delete newline spacer tags from the text view instead and then save. It appears that changes are only saved if you press the save button while in text view. Pressing save while in code view.
```html
<p>
  <br>
</p>
```
&emsp; Example [recipe](/recipes/webparts/#title-text-statement)

#### Text Caveats

&emsp; Because we can just create HTML from the text view, it might seem all-powerful, however, all it takes is one user to *Edit* and *Republish* the page on SharePoint to remove all of your tags and info that is not `<p>` or `<br>` tags.

### Title

&emsp; This is like the title part of many web parts. In *Edit widget*, to prevent redundant titles, we recommend setting the top *Title* to *Hidden* in the *Chrome type* dropdown.

&emsp; Example [recipe](/recipes/webparts/#title-text-statement)

---

## Edit Widget Explanations

### Search Query

&emsp; In Powell, you may have seen this Search query box, called either *Search query* or *Search query template*:

![search query](https://i.postimg.cc/xC8js7F2/search-query.png)

The language used in this particular search box is [Keyword Query Language (KQL)](https://learn.microsoft.com/en-us/sharepoint/dev/general-development/keyword-query-language-kql-syntax-reference). KQL is used to build search queries for the SharePoint search service. For syntax and more, please refer to documentation [here](https://learn.microsoft.com/en-us/sharepoint/dev/general-development/building-search-queries-in-sharepoint). These search queries allow developers to query the SharePoint site, often times for looking for info in site contents.

Keep in mind that there is an entirely separate query language with the same acronym that Microsoft uses for Azure called Kusto Query Language (KQL). This is *not* used in SharePoint.

#### [KQL Cheat Sheet](https://www.sharepointagency.co.nz/consulting/blog-search/item/350-keyword-query-language-kql-cheat-sheet.html)

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

### Avoid Nesting Folders in SharePoint Sites

&emsp; Folders as seen on the *site contents* level in the SharePoint site are special folders called *Document Library* folders. If we want to limit grabbing items from a specific folder can only limit the scope of information grabbed by Document Library folders. The same information will be grabbed at the Document Library level folder will be grabbed from the nested folder. Nested folders do not help with organization. Only keep files and lists folders for content in Powell. Do not use folders within folders.

### Form View

&emsp; You may be tempted to use:

`PATH: "https://unifiedphysicianmgt.sharepoint.com/sites/UnifiedWomensHealth/Communications"`

but we actually need to use

`PATH: "https://unifiedphysicianmgt.sharepoint.com/sites/UnifiedWomensHealth/Communications/Forms"`

because we need the Forms view of the files.

### Row limit
&emsp; Think of a SharePoint list. Each row in this case is an item on the list. Therefore, row limit really means item limit.

**Example**

&emsp; In the [grid list of links recipe](/recipes/webparts/#grid-list-of-links), we want an arbitrary max of 27 rows or 27 items that will be grabbed from the SharePoint List

---

## Display or Select Widgets

&emsp; When building a webpart, there is often a secondary choice of the Display widget. Not all webparts have display widgets. For example, the [discussion tiles webpart](#discussion-tiles) cannot display a specific widget other than what it comes with.

### Species

#### Application Tiles 2

TODO

---

## Tips and Tricks

### Determine the Type of Webpart By Inspecting SharePoint Site with Dev Tools

&emsp; The type of webpart can be found in the `data-sp-feature-tag`. You'll want to inspect the page, and press `Ctrl + F` to find this attribute in the HTML. It may look like the following:
```html
<div data-sp-feature-tag="PowellScriptEditorWebPart web part (Search)" ...>...</div>
```
The webpart featured here is *Search*.
