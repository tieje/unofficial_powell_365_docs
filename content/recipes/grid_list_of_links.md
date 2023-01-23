+++
title = "Grid List of Links"
insert_anchor_links = "right"
+++

![grid-list-links.png](https://i.postimg.cc/xC7JWZMN/grid-list-links.png)

TL:DR;
> "use graph webpart and then application tiles widget view and set 3 per row"
>
> ~ <cite>Dah Master</cite>&emsp;![dah master](https://avatars.githubusercontent.com/u/53357172?s=64&v=4)

## Table of Contents
- [Table of Contents](#table-of-contents)
- [What We Are Making](#what-we-are-making)
- [In Powell Manager](#in-powell-manager)
  - [Create a Custom Content Type](#create-a-custom-content-type)
  - [Create a List Template](#create-a-list-template)
  - [Create new List from List Template](#create-new-list-from-list-template)
  - [Add to Site Template](#add-to-site-template)
- [In SharePoint Site Contents](#in-sharepoint-site-contents)
  - [Create Items For the List](#create-items-for-the-list)

## What We Are Making

&emsp; A list of accessible links is one of the most commonly requested requirements that clients ask for in SharePoint sites. To create this grid style list of links with icons, perform the following steps.

## In Powell Manager

### Create a Custom Content Type

&emsp; Here, we will be creating a custom content type that inherits from the standard Item Content Type. It will contain additional fields for image, number, and URL.

1. [Go to content types](/actions/common/#powell-intranet-content-types)
2. *Create a new content type*
3. Name your new content type. Inherit from *Item* Content Type. Save.
4. You should be in edit mode for your new content Type. Go to *Fields*
5. *Add new field*
6. *Create a new field*. Name your fields appropriately.
   1. Create an image field: *Select a field type*, choose Image.
   2. Create a number field: *Select a field type*, choose Number.
   3. Create a URL field: *Select a field type*, choose URL.
7. Save

### Create a List Template

&emsp; In Powell Manager, the list template is used by the web part widget. If you already have this list template, then you can skip this section.

1. [Go to list templates](/actions/common/#powell-intranet-list-templates)
2. *Create a new list template*
3. Fill in *Title*. *Select a list template model to inherit from* dropdown, select *Generic List*
4. *Content Types*
5. *Add a new content type*
6. *Add an existing content type*
7. Under *Custom content types*, choose [the custom content type that you created](#create-a-custom-content-type). *Add* it
8. Save

### Create new List from List Template

1. [Get to your site](/actions/common/#powell-intranet-your-site)
2. *Lists* (left sidebar)
3. *Create a new list*
4. Fill in *Title*. Under *Select a list model* dropdown, select [the list template that you created](#create-a-list-template) under *My List Templates*
5. Save and Sync

### Add to Site Template

1. [Get to your site](/actions/common/#powell-intranet-your-site)
2. *Pages* on the left column
3. Edit button for the page that you want to edit
4. Scroll to the bottom under *Placeholder Main*. `Add a webpart`
   - If you need to add a space on your site for the web part, edit the template under the `Selected Page Layout` 
5.  Use the `Graph` web part
6. Scroll down to `Display`
7. `Select a widget view`
8. Use the `Application Tiles` widget
9. Set the following
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

## In SharePoint Site Contents 

### Create Items For the List

1. The (+) sign next to the gear wheel,
2. Choose [the list that you created](#create-new-list-from-list-template)
3. Fill in the fields.
4. Create as many items in the list as needed.
