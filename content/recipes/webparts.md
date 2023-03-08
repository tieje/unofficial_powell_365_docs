+++
title = "Recipes for Webparts"
+++

---

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Intro](#intro)
- [Grid List of Links](#grid-list-of-links)
  - [What We Are Making](#what-we-are-making)
  - [In Powell Manager](#in-powell-manager)
    - [Create a Custom Content Type](#create-a-custom-content-type)
    - [Create a List Template](#create-a-list-template)
    - [Create new List from List Template](#create-new-list-from-list-template)
    - [Add to Site Template](#add-to-site-template)
  - [In SharePoint Site Contents](#in-sharepoint-site-contents)
    - [Create Items For the List](#create-items-for-the-list)
- [Combined Search Videos](#combined-search-videos)
  - [What We Are Making](#what-we-are-making-1)
  - [In Powell Manager](#in-powell-manager-1)
    - [Add to Site Template](#add-to-site-template-1)
  - [In SharePoint Site Contents](#in-sharepoint-site-contents-1)
    - [Create Videos Files](#create-videos-files)
- [Title Text Statement](#title-text-statement)
  - [What We Are Making](#what-we-are-making-2)
  - [In Powell Manager](#in-powell-manager-2)
    - [Add to Site Template](#add-to-site-template-2)

---

## Intro

&emsp; Webparts are the basic building blocks of SharePoint sites. Below are "recipes" on how to build specific web components in Powell for SharePoint Sites. For more information on Webparts, you can check the reference [here](/references/webparts).

---

## Grid List of Links

![grid-list-links.png](https://i.postimg.cc/xC7JWZMN/grid-list-links.png)

TL:DR;
> "use graph webpart and then application tiles widget view and set 3 per row"
>
> ~ <cite>Dah Master</cite>&emsp;![dah master](https://avatars.githubusercontent.com/u/53357172?s=40&v=4)

### What We Are Making

&emsp; A list of accessible links is one of the most commonly requested requirements that clients ask for in SharePoint sites. To create this grid style list of links with icons, perform the following steps.

### In Powell Manager

#### Create a Custom Content Type

&emsp; Here, we will be creating a custom content type that inherits from the standard Item Content Type. It will contain additional fields for image, number, and URL.

1. [Create a new item content type](/actions/common/#powell-intranet-create-a-content-type-that-inherits-from-item)
   1. Create an image field: *Select a field type*, choose Image.
   2. Create a number field: *Select a field type*, choose Number.
   3. Create a URL field: *Select a field type*, choose URL.
6. Save

#### Create a List Template

&emsp; In Powell Manager, the list template is used by the web part widget. If you already have this list template, then you can skip this section.

1. [Create a new list template](/actions/common/#powell-intranet-create-a-new-list-template)
2. *Select a list template model to inherit from* dropdown, select *Generic List*
3. *Content Types*
4. *Add a new content type*
5. *Add an existing content type*
6. Under *Custom content types*, choose [the custom content type that you created](#create-a-custom-content-type). *Add* it
7. Save

#### Create new List from List Template

1. [Create a new list](/actions/common/#powell-intranet-create-a-new-list)
2. Under *Select a list model* dropdown, select [the list template that you created](#create-a-list-template) under *My List Templates*
3. Save and Sync

#### Add to Site Template

1. [Add a Webpart](/actions/common/#powell-intranet-add-a-webpart)
2. Use the *Graph* web part
3. Scroll down to *Display*
4. *Select a widget view*
5. Use the *Application Tiles* widget
6. Set the following
   1. *Title*
   2. *Site Url* to your sharepoint site Url
   3. *List* to *Manual value*. Type in [the list that you created](#create-new-list-from-list-template)
   4. *Sort Property* to the *Internal Name* of [the *number* field of your custom content type](#create-a-custom-content-type)
   5. *Sort Direction* descending or whichever you prefer
   6. [*Row Limit*](/references/webparts/#row-limit) to however many rows you want to limit to. For example, three pages of 3x3 items, we would want 27. The following are recommended numbers, but do what fits your needs:
      1. *Mobile item's per row* to 2
      2. *Tablet item's per row* to 2
      3. *Desktop item's per row* to 3
      4. *Large screen item's per row* to 3
   7. Under *Mapping*
      1. Choose *Map as Publishing Field*, for *title*, type *Title*
      2. Choose *Map as Publishing Field*, for your custom image field, type its internal name
      3. Choose *Map as Publishing Field*, for your custom number field, type its internal name
      4. Choose neither checkbox, for your custom URL field, type its internal name
   8. Save and Sync

### In SharePoint Site Contents 

#### Create Items For the List

1. The (+) sign next to the gear wheel,
2. Choose [the list that you created](#create-new-list-from-list-template)
3. Fill in the fields.
4. Create as many items in the list as needed.

---

## Combined Search Videos

![combined-search-videos.png](https://i.postimg.cc/WbRtkTHF/combined-search-videos.png)

TL:DR;
> "use `FileType: mp4` search query"
>
> ~ <cite>a Student</cite>&emsp;![a student](https://avatars.githubusercontent.com/u/19988117?s=40&v=4)

### What We Are Making

&emsp; A list of videos as part of a [combined search webpart](/references/webparts/#combined-search-web-part). You may wish to [create the videos files](#create-videos-files) first because the [search query](/references/webparts/#search-query) might be based on where you stored your videos in storage.

### In Powell Manager

#### Add to Site Template

1. [Add a Webpart](/actions/common/#powell-intranet-add-a-webpart)
2. Use the *Combined search* webpart
3. Scroll down to *Configuration*
4. *Select a widget view*
5. In our case, we will be using the *Vertical* widget, but feel free to use what you need.
6. Set the following:
   1. *Title*
7. *New Configuration*. Set the following:
   1. *Title*
   2. [*Search query template*](/references/webparts/#search-query)
   3. [Row limit](/content/references/webparts/#row-limit)
   4. *Display* -> *Select a display type* -> *Select a widget view*
   5. Under *Must read items*, set the following to your needs or the following parameters
      1. *Mobile item's per row* to 1
      2. *Tablet item's per row* to 1
      3. *Desktop item's per row* to 4
      4. *Large screen item's per row* to 4
8.  Save the Configuration
9.  Save the Webpart
10. Save the page template
11. Sync the Webpart
12. Go back to *Edit Site Template*
13. Save all site templates.
14. Sync the site template that you were working on.

### In SharePoint Site Contents 

&emsp; If you do not have any content to upload, I recommend downloading sample video content from [here](https://samplelib.com/sample-mp4.html).

#### Create Videos Files

1. [Go to site contents](/actions/common/#site-contents)
2. Create a Document Library Folder with the same name as what [you specified in your search query](#add-to-site-template)
3. *New*. Choose from your computer and upload the sample video files

---

## Title Text Statement

![title text statement](https://i.postimg.cc/mrZm2J5T/title-text-statement.png)

### What We Are Making

&emsp; A paragraph with a mission statement and title with horizontal dividers. This turns out to be a web part with many pieces.

### In Powell Manager

#### Add to Site Template

1. [Add the following Webparts to a single zone](/actions/common/#powell-intranet-add-a-webpart)
   1. *Title*
      1. Set *Chrome type* for title to *hidden*
   2. *Divider*
   3. *Text*
      1. Set font size to 30 and alignment center
   4. *Divider*
2. [Add the following code to Custom CSS](/actions/common/#powell-intranet-custom-css)
```css
hr[role="presentation"] {
    color: #981d97;
}
```
