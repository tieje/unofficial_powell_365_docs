+++
title = "Recipes for Entire Powell Web Pages"
+++

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Powell Example Web Pages](#powell-example-web-pages)
- [Waterfountain Page](#waterfountain-page)
  - [What We Are Making](#what-we-are-making)
  - [In Powell Manager](#in-powell-manager)
    - [Create a Custom Content Type](#create-a-custom-content-type)
    - [Create a List Template](#create-a-list-template)
    - [Create new List from List Template](#create-new-list-from-list-template)
    - [Create the Page](#create-the-page)
    - [Add to Site Template](#add-to-site-template)
  - [In SharePoint Site Contents](#in-sharepoint-site-contents)
    - [Create Items For the List](#create-items-for-the-list)

## Powell Example Web Pages

&emsp; There exists a [sample Powell SharePoint site](https://pow365.sharepoint.com/sites/multilingualconnect/en-US/) with several examples of Powell webparts. You can request access [here](https://support.powell-software.com/hc/en-us/requests/new). Unfortunately, getting access to the Powell Manager which shows its settings, has not been possible, at least to our knowledge. For this reason, this section was created to show how to build these pages.

## Waterfountain Page

| ![water-fountain-top-half.png](https://i.postimg.cc/wTwTvy79/water-fountain-top-half.png) |
|:---:|
| **Top Half** |

| ![water-fountain-bottom-half.png](https://i.postimg.cc/BQbfmhnG/water-fountain-bottom-half.png) |
|:---:|
| **Bottom Half** |

TL:DR;
> "search webpart and discussion tiles webpart"
>
> ~ <cite>a Student</cite>&emsp;![a student](https://avatars.githubusercontent.com/u/19988117?s=40&v=4)

> "Create a page layout, create a page template, create a page in site template"
>
> ~ <cite>Dah Master</cite>&emsp;![dah master](https://avatars.githubusercontent.com/u/53357172?s=40&v=4)

### What We Are Making

&emsp; We will be making a water fountain page, which can be found in the Powell example site [here](https://pow365.sharepoint.com/sites/multilingualconnect/en-US/waterfountain). We can determine the type of the webparts by [looking for the the `data-sp-feature-tag`](/actions/common/#search-for-a-tag-or-attribute-on-a-web-page) on the [example water fountain page](/references/webparts/#determine-the-type-of-webpart-by-inspecting-sharepoint-site-with-dev-tools). There are main webparts for this page:

1. Search
2. Discussion tiles

### In Powell Manager

#### Create a Custom Content Type

&emsp; Here, we will be creating a custom content type that inherits from the standard Item Content Type. It will contain additional fields for image, number, and URL.

1. [Create a new item content type](/actions/common/#powell-intranet-create-a-content-type-that-inherits-from-item)
   - Create a URL field: *Select a field type*, choose URL.
2. Save

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

#### Create the Page

1. [Create a new page for you site](powell-intranet-create-a-new-page-for-your-site)
   - For page template
     - Under *Page header*, choose *No header*
     - Under Select page content type, choose *Waterfountain topic*
2. Under *Placeholder Main*, *Add a webpart*, choose the *Search* webpart.
3. Set the following fields:
   - *Title*: `Find a conversation topic to engage a discussion with your colleagues`
   - Under *Query Builder*, fill in *Search query template* with the following query:
     - ``
   - [*Row limit*](/references/webparts/#row-limit): `12` or whatever suits your needs
   - Under *Display*, *Select a widget view*, choose *Application Tiles 2*
   - 

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

