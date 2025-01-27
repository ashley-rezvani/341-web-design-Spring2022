---
title: Boxing Sizing
module: topic-11
permalink: /topic-11/box-sizing/
---

<div class="divider-heading"></div>

<img src="../img/box-model-content.gif" alt="drawing basic boxes" style="width: 350px; margin: 0 auto 30px;" />

There are a number of ways to control the **size** of boxes. The first two properties you already know well are aptly named `width: ` and `height: `.

As with properties affecting typography, there are ways of setting the size of boxes using both absolute and relative measurement values.


<h3>Absolute Sizes</h3>

<div class="code-heading">
  <span class="css">CSS</span>
</div>
```css
.my-box {
  width: 100px;
  height: 50px;
}
```

The advantage of 'hard-coding' the size of elements to absolute values using pixels is that you know _exactly_ how the site will look. The relationships of elements to each other will stay the same, and never change. Of course, this may lose impact if the screen size of the viewer's device is not large enough to see all of the content, and they are forced to awkwardly scroll around.

This may also get slightly askew when your user increases or decreases the font size of page which will cause the boxes to increase/decrease as well.

That being said, there are times when using pixels is appropriate.

<div class="codepen-embed">
  <p data-height="400" data-theme-id="30567" data-slug-hash="GRqxVEV" data-default-tab="css,result" data-user="retrog4m3r" data-embed-version="2" data-pen-title="Box Models, Pt. 1" class="codepen"></p>
</div>

<h3>Relative Sizes</h3>

<div class="code-heading">
  <span class="css">CSS</span>
</div>
```css
.my-box {
  width: 100%;
  height: 50%;
}
```

Another way of specifying size of boxes is through percentages. Percentages are relational to the percent specified in the _parent_ element.

If the parent element is `<body>...</body>` then the elements width can be set using a percentage, and it will stay in relation to the size of the page. However, the height must be set using an absolute value still.

In the following example, the parent-container or outer-box is set to be 66% the width of the window or parent example container in this example. There is no height property given. So instead, it is made tall enough by the browser to hold its content.

The 'inner-box' is set to be 75% of the width, and 50% of the height of the 'parent-container.'

<div class="codepen-embed">
  <p data-height="400" data-theme-id="30567" data-slug-hash="oNLqKeQ" data-default-tab="css,result" data-user="retrog4m3r" data-embed-version="2" data-pen-title="Box Models, Pt. 2" class="codepen"></p>
</div>


<h3 id="combine-size">Combining Size Types</h3>

<div class="code-heading">
  <span class="css">CSS</span>
</div>
```css
.my-box {
  width: 100%;
  height: 50px;
}
```

Now that our boxes can resize in relation to the screen using _relative_ values, we will have to be careful about setting absolute sizes, but it can be done in certain contexts.

The following is the same example as the previous <u>except</u> the height of the 'parent-container' is set to 300px. There is also more text. Notice that when you make your browser window narrow, the text spills out of the element. _This is an example of bad web design._

<div class="codepen-embed">
  <p data-height="600" data-theme-id="30567" data-slug-hash="MWeVNEv" data-default-tab="css,result" data-user="retrog4m3r" data-embed-version="2" data-pen-title="Box Models, Pt. 3" class="codepen"></p>
</div>
