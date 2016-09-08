Fonts
=====

If you want to use webfonts in a PDF, you will need to embed the webfont ttf in the css (using truetype is important). Options:
  - put the base64-encoded file directly in the css
   ```
   @font-face {
     font-family: 'FontAwesome';
     src: url(data:font/truetype;charset=utf-8;base64,BASE64_STRING_HERE) format('truetype');
     font-weight: normal;
     font-style: normal;
   }
   ```
  - if using webpack, use [`base64-font-loader`](https://github.com/nicksrandall/base64-font-loader), but be careful
  when configuring webpack as you don't want to do this for your normal web build

