+++
title = "Navigation"
+++

---

## Table of Contents
- [Table of Contents](#table-of-contents)
- [Design Home Navigation](#design-home-navigation)
  - [Create a new node](#create-a-new-node)
    - [navigation section with static sublinks](#navigation-section-with-static-sublinks)
    - [static link](#static-link)
    - [search query](#search-query)
    - [connected users groups](#connected-users-groups)
    - [Example](#example)

---

## Design Home Navigation

### Create a new node
&emsp; *Creating a new node* creates a new navigation link in the nav bar. This navigation link can be one of the following *Link type*s:

#### navigation section with static sublinks

&emsp; An element that produces a dropdown list of links upon hovering. Hovering on this element opens its menu of links or sub-links. As soon as the node underneath this is a [static link](#static-link), it is no longer possible to add additional sub-links. Complex sub link trees are not possible. Max one nesting of links in a sub-link is recommended.

#### static link

&emsp; A simple link, the same as clicking on an anchor tag.

#### search query

TODO

#### connected users groups

TODO

#### Example

&emsp; If we wanted a navigation like this, we would want to :

node type | [static](#static-link) | [section with static sublink](#navigation-section-with-static-sublinks) | [section with static sublink](#navigation-section-with-static-sublinks)
:---: | :---: | :---: | :---:
Headers | Home | About Us | Contact Us
static Link 1 | no link | Our Company | Set up Appointment
static Link 2 | no link | Our Staff | Call Us

The rest of the links under the headers would be [static](#static-link).
