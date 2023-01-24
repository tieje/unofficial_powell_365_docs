+++
title = "Combined Search Videos"
+++

![combined-search-videos.png](https://i.postimg.cc/WbRtkTHF/combined-search-videos.png)

TL:DR;
> "use `FileType: mp4` search query"
>
> ~ <cite>a Student</cite>&emsp;![dah master](https://avatars.githubusercontent.com/u/19988117?s=40&v=4)

## Table of Contents
- [Table of Contents](#table-of-contents)
- [What We Are Making](#what-we-are-making)
- [In Powell Manager](#in-powell-manager)
  - [Add to Site Template](#add-to-site-template)
- [In SharePoint Site Contents](#in-sharepoint-site-contents)
  - [Create Videos Files](#create-videos-files)

## What We Are Making

&emsp; A list of videos as part of a [combined search webpart](/references/webparts/#combined-search-web-part). You may wish to [create the videos files](#create-videos-files) first because the [search query](/references/webparts/#search-query) might be based on where you stored your videos in storage.

## In Powell Manager

### Add to Site Template

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

## In SharePoint Site Contents 

&emsp; If you do not have any content to upload, I recommend downloading sample video content from [here](https://samplelib.com/sample-mp4.html).

### Create Videos Files

1. [Go to site contents](/actions/common/#site-contents)
2. Create a Document Library Folder with the same name as what [you specified in your search query](#add-to-site-template)
3. *New*. Choose from your computer and upload the sample video files
