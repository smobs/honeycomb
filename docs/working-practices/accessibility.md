---
layout: default
section: working-practices
title: Accessibility
---

## Contents

* Will be replaced with the ToC
{:toc}


## People
Accessibility matters, it matters to those trying to use our software with a disability, it's in our contracts, it also directly relates to discrimination laws we need to know about, as well as simply being the right thing to do.

Writing semantic HTML, CSS that's flexible with layout & font-size as well as using Javascript to add keyboard support go a long way in making a web app as accessible as possible.

It's not always difficult to make something accessible.  Always ask what you can do to improve a pages accessibility.

## Visual impairments
Supporting blind users of screen reading software like JAWS / NVDA is the obvious case but there are others.  Use a sensibly sized default font and provide alt stylesheets for different font sizes. Use enough contrast between colours and foreground / background to enhance readability.

Use a screen reader, it's the only way to gain a good insight into what using our software is really like for blind users.

## Accessible tables & forms
Keep tables simple and avoid nested headings. Using th elements for heading cells with appropriate scope is the first step for accessible tables.

``` html
<table>
	<tr>
        <th scope="col">Name</th>
		<th scope="col">Age</th>
		<th scope="col">Birthday</th>
	</tr>
	<tr>
		<th scope="row">Jackie</th>
		<td>5</td>
		<td>April 5</td>
	</tr>
	<tr>
		<th scope="row">Beth</th>
		<td>8</td>
		<td>January 14</td>
	</tr>
</table>
```

Linking labels to inputs with the for attribute is the first step for accessible forms.

``` html
<label for="email">Email</label>
<input id="email">
```

Resources:

* [http://www.456bereastreet.com/archive/200410/bring_on_the_tables/](http://www.456bereastreet.com/archive/200410/bring_on_the_tables/)
* [http://www.webstandards.org/learn/tutorials/accessible-forms/](http://www.webstandards.org/learn/tutorials/accessible-forms/)

## Motor impairments
Most of us can appreciate using keyboard short cuts for navigating forms, people with low mobility will appreciate being able to use our software without a mouse far more than this.

## UI consistency
This one is not as obvious as the other points, but is as valid.  A consistent UI will help all our users be able to access what they need to.  It's rare to find a web application of our size and complexity that doesn't have a style guide, let's make one.

## WCAG <span class="amp">&</span> WAI ARIA
We have focused on <abbr title="Web Content Accessibility Guidelines">WCAG</abbr> 1 Level A compliance in the past, <abbr title="Web Accessibility Initiative’s Accessible Rich Internet Applications">WAI ARIA</abbr> is a fairly recent addition and focuses on the moving parts of a web app. The ARIA attributes can help explain dynamic changes to the page with javascript to users of assistive technologies.

[http://dev.opera.com/articles/view/introduction-to-wai-aria/](http://dev.opera.com/articles/view/introduction-to-wai-aria/)

## Best practices:

* Test in JAWS or NVDA (onch U:) - Add alt attributes, accessible forms & tables
* Consider Ajax & screen readers - How do you alert users to changed content?
* Add keyboard alternatives to all mouse events - mouseover -> focus, mouseout -> blur - Test without a mouse
* Assistive features - High contrast stylesheet, font-size stylesheets, access keys, skip links
* Avoid colour alone for critical information - e.g. Red = bad, Green = good
* Help everyone - Usable in different screen sizes, consistent navigation and user experience, friendly URLs, favicon etc.


People to follow:

[@jkiss](http://twitter.com/jkiss/)
[@stevefaulkner](http://twitter.com/stevefaulkner/)
[@vick08](http://twitter.com/vick08/)
