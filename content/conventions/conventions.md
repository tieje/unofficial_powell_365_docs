+++
title = "Conventions"
insert_anchor_links = "right"
weight = 1
+++

---

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Purpose](#purpose)
- [Note to Contributors](#note-to-contributors)
- [Problem Solving Methods](#problem-solving-methods)
  - [For Building Web Components](#for-building-web-components)
- [FAQs](#faqs)
  - [What is the difference between sync and save in Powell Intranet](#what-is-the-difference-between-sync-and-save-in-powell-intranet)
  - [Where to implement Custom CSS](#where-to-implement-custom-css)

---

## Purpose

&emsp; Because Powell is low-code/no-code solution, it requires what some call may *tribal knowledge*. This section contains justifications and guides of why things should be done a certain way and how to do them in Powell.

---

## Note to Contributors

&emsp; For contributors, this section should be referenced often for why things are done a certain way.

---

## Problem Solving Methods

### For Building Web Components

1. Understand the Webpart and, if needed, the Display widget that you are using.
   - [Not all webparts use a custom Display widget](/references/webparts/#display-or-select-widget).
   - Which field types will the Display widget need?
2. Create the content type.
3. Create the list template.
4. Create the list.
5. Add the webpart.
6. Save and Sync.

If you have any questions, reach out to Powell Support ASAP. They will probably answer on the same day, but it may take a day or two for them to set up a meeting.

---

## FAQs

### What is the difference between sync and save in Powell Intranet

&emsp; [*Save*](/references/definitions/#save) saves the configuration to Powell Manager. [*Sync*](/references/definitions/#sync) creates a deployment task to the tenant. The proper steps of the process of the process are always:
1. Save
2. Sync

### Where to implement Custom CSS
&emsp; [Go to Custom CSS](/actions/common/#powell-intranet-custom-css). There is an editor there, but I recommend copying and pasting from a real code editor like [VSCode](https://code.visualstudio.com/). Remember to save and sync.

