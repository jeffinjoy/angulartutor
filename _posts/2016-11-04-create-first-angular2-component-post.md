---
layout: post
title: Create your first angular2 component
description: "Demo post displaying the various ways of highlighting code in Markdown."
modified: 2016-11-03T15:27:45-04:00
tags: [sample post, code, highlighting]

---

In Angular 2, Components are the main way we build and specify elements and logic on the page.

In Angular 1, we achieved this through directives, controllers, and scope. In Angular 2, all those concepts are combined into Components.

A SIMPLE COMPONENT

Here’s a simple Component that renders our name, and a button that triggers a method to print our name to the console:

---javascript

import { Component } from '@angular/core';

@Component({
  selector: 'my-component',
  template: '<div>Hello my name is {{name}}. <button (click)="sayMyName()">Say my name</button></div>'
})
export class MyComponent {
  constructor() {
    this.name = 'Max'
  }
  sayMyName() {
    console.log('My name is', this.name)
  }
}

When we use the <my-component></my-component> tag in our HTML, this component will be created, our constructor called, and rendered.
