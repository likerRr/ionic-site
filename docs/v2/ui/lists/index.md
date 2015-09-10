---
layout: v2/docs_ui
title: Ionic 2 UI | Lists
header_title: Lists - Ionic 2 UI
header_sub_title: Ionic 2 Developer Preview
---

<h1 class="title">Lists</h1>

Lists are used to display rows of information, such as a contact list,
playlist, or menu. Or maybe something crazy we don't even know exists yet!


<div class="demo">
  <iframe src="/dist/examples/list/basic/"></iframe>
  <a href="https://github.com/driftyco/ionic2/tree/master/ionic/components/list/test/basic">See demo source <i class="icon ion-ios-arrow-right"></i></a>
</div>


```html
<ion-list>
  <ion-item *ng-for="#item of items" (^click)="itemSelected(item)">
    {{item.title}}
  </ion-item>
</ion-list>
```

By default, lists have an outside margin, to remove that add the `inset` property
to make the list flush with the parent container.

### Virtual Scrolling (Experimental)

Virtual Scrolling (previously known as Collection Repeat) makes it possible to scroll through
massive lists without any slow downs.

To enable it, set the `virtual` property on the list, as well as providing a
reference to an array of items, and the parent scroll element:

```html
<ion-content #content>
  <ion-list inset virtual [items]="items" [content]="content">
  </ion-list>
</ion-content>
k```