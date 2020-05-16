# hn_dark
Dark color theme for Hacker News

## Experiment with custom CSS on any Hacker News page
1. Copy the code sample below and paste it into your browser console.
2. Take your custom CSS and paste immediately below the comment in the code sample.
3. Press *enter* on your keyboard.

```javascript
var makedark = function (css) {var oldStyle=document.getElementsByTagName("style")[0],style=document.createElement("style");if (oldStyle!==undefined){oldStyle.parentNode.removeChild(oldStyle);}style.setAttribute("type", "text/css");style.innerHTML=css;document.getElementsByTagName("head")[0].appendChild(style);document.getElementsByTagName("body")[0].setAttribute("class", "dark")};makedark(`

//paste css code below this line:


`);
```

## Example using this CSS code:

```javascript
var makedark = function (css) {var oldStyle=document.getElementsByTagName("style")[0],style=document.createElement("style");if (oldStyle!==undefined){oldStyle.parentNode.removeChild(oldStyle);}style.setAttribute("type", "text/css");style.innerHTML=css;document.getElementsByTagName("head")[0].appendChild(style);document.getElementsByTagName("body")[0].setAttribute("class", "dark")};makedark(`

//paste css code below this line:
body,
td,
.default,
.admin,
.title,
.subtext,
.yclinks,
.pagetop,
.comhead,
.comment,
.admin td,
.subtext td,
input[type=\"submit\"] { font-family:Verdana, Geneva, sans-serif; }

body,
td,
.default,
.pagetop,
.title { font-size:10pt; }

.admin,
.admin td   { font-size:8.5pt; }

.subtext,
.subtext td { font-size:7pt; }

.comhead,
.yclinks { font-size:8pt; }

.comment { font-size:9pt; }

textarea,
input { font-family:monospace; font-size:10pt; }

a:link,
a:visited { text-decoration:none; }

.hnname  { margin-right: 5px; }

.noshow { display: none; }
.nosee { visibility: hidden; pointer-events: none; cursor: default }

.comment a:link,
.comment a:visited,
.subtext a:hover,
.comhead a:hover,
.hnmore { text-decoration:underline; }

.default p { margin-top: 8px; margin-bottom: 0px; }

.pagebreak {page-break-before:always}

pre { overflow: auto; padding: 2px; }
pre:hover { overflow:auto }

.votearrow {
  width:      10px;
  height:     10px;
  border:     0px;
  margin:     3px 2px 6px;
  background: url("grayarrow.gif")
  no-repeat;
}

.votelinks.nosee div.votearrow.rotate180 {
  display: none;
}

@media only screen and (-webkit-min-device-pixel-ratio: 2), only screen and (min-device-pixel-ratio: 2) {
  .votearrow { background-size: 10px; background-image: url("grayarrow2x.gif"); }
}

.rotate180 {
  -webkit-transform: rotate(180deg);  /* Chrome and other webkit browsers */
  -moz-transform:    rotate(180deg);  /* FF */
  -o-transform:      rotate(180deg);  /* Opera */
  -ms-transform:     rotate(180deg);  /* IE9 */
  transform:         rotate(180deg);  /* W3C complaint browsers */

  /* IE8 and below */
  -ms-filter: "progid:DXImageTransform.Microsoft.Matrix(M11=-1, M12=0, M21=0, M22=-1, DX=0, DY=0, SizingMethod='auto expand')";
}

/* mobile device */
@media only screen
and (min-width : 300px)
and (max-width : 750px) {
  #hnmain { width: 100%; }
  body { padding: 0; margin: 0; width: 100%; -webkit-text-size-adjust: none; }
  td { height: inherit !important; }
  .title, .comment { font-size: inherit;  }
  span.pagetop { display: block; margin: 3px 5px; font-size: 12px; }
  span.pagetop b { display: block; font-size: 15px; }
  table.comment-tree .comment a { display: inline-block; max-width: 200px; overflow: hidden; white-space: nowrap;
    text-overflow: ellipsis; vertical-align:top; }
  img[src='s.gif'][width='40'] { width: 12px; }
  img[src='s.gif'][width='80'] { width: 24px; }
  img[src='s.gif'][width='120'] { width: 36px; }
  img[src='s.gif'][width='160'] { width: 48px; }
  img[src='s.gif'][width='200'] { width: 60px; }
  img[src='s.gif'][width='240'] { width: 72px; }
  img[src='s.gif'][width='280'] { width: 84px; }
  img[src='s.gif'][width='320'] { width: 96px; }
  img[src='s.gif'][width='360'] { width: 108px; }
  img[src='s.gif'][width='400'] { width: 120px; }
  img[src='s.gif'][width='440'] { width: 132px; }
  img[src='s.gif'][width='480'] { width: 144px; }
  img[src='s.gif'][width='520'] { width: 156px; }
  img[src='s.gif'][width='560'] { width: 168px; }
  img[src='s.gif'][width='600'] { width: 180px; }
  img[src='s.gif'][width='640'] { width: 192px; }
  img[src='s.gif'][width='680'] { width: 204px; }
  img[src='s.gif'][width='720'] { width: 216px; }
  img[src='s.gif'][width='760'] { width: 228px; }
  img[src='s.gif'][width='800'] { width: 240px; }
  img[src='s.gif'][width='840'] { width: 252px; }
  .title { font-size: 11pt; line-height: 14pt;  }
  .subtext { font-size: 9pt; }
  .itemlist { padding-right: 5px;}
  .votearrow { transform: scale(1.3,1.3); margin-right: 6px; }
  .votearrow.rotate180 {
    -webkit-transform: rotate(180deg) scale(1.3,1.3);  /* Chrome and other webkit browsers */
    -moz-transform:    rotate(180deg) scale(1.3,1.3);  /* FF */
    -o-transform:      rotate(180deg) scale(1.3,1.3);  /* Opera */
    -ms-transform:     rotate(180deg) scale(1.3,1.3);  /* IE9 */
    transform:         rotate(180deg) scale(1.3,1.3);  /* W3C complaint browsers */
  }
  .votelinks { min-width: 18px; }
  .votelinks a { display: block; margin-bottom: 9px; }
  input[type='text'], input[type='number'], textarea { font-size: 16px; width: 90%; }
}

.comment { max-width: 1215px; overflow: hidden }
pre { max-width: 900px; }

@media only screen and (min-width : 300px) and (max-width : 389px) {
  .comment { max-width: 270px; overflow: hidden }
  pre { max-width: 200px; }
}
@media only screen and (min-width : 390px) and (max-width : 509px) {
  .comment { max-width: 350px; overflow: hidden }
  pre { max-width: 260px; }
}
@media only screen and (min-width : 510px) and (max-width : 599px) {
  .comment { max-width: 460px; overflow: hidden }
  pre { max-width: 340px; }
}
@media only screen and (min-width : 600px) and (max-width : 689px) {
  .comment { max-width: 540px; overflow: hidden }
  pre { max-width: 400px; }
}
@media only screen and (min-width : 690px) and (max-width : 809px) {
  .comment { max-width: 620px; overflow: hidden }
  pre { max-width: 460px; }
}
@media only screen and (min-width : 810px) and (max-width : 899px) {
  .comment { max-width: 730px; overflow: hidden }
  pre { max-width: 540px; }
}
@media only screen and (min-width : 900px) and (max-width : 1079px) {
  .comment { max-width: 810px; overflow: hidden }
  pre { max-width: 600px; }
}
@media only screen and (min-width : 1080px) and (max-width : 1169px) {
  .comment { max-width: 970px; overflow: hidden }
  pre { max-width: 720px; }
}
@media only screen and (min-width : 1170px) and (max-width : 1259px) {
  .comment { max-width: 1050px; overflow: hidden }
  pre { max-width: 780px; }
}
@media only screen and (min-width : 1260px) and (max-width : 1349px) {
  .comment { max-width: 1130px; overflow: hidden }
  pre { max-width: 840px; }
}

/* ------ colors ------ */

/* default colors */
body { color:#828282; }
td { color:#828282; }
.admin td { color:#000000; }
.subtext td { color:#828282; }
a:link    { color:#000000; }
a:visited { color:#828282; }
.default { color:#828282; }
.admin   { color:#000000; }
.title   { color:#828282; }
.subtext { color:#828282; }
.yclinks { color:#828282; }
.pagetop { color:#222222; }
.comhead { color:#828282; }
.c00, .c00 a:link { color:#000000; }
.c5a, .c5a a:link, .c5a a:visited { color:#5a5a5a; }
.c73, .c73 a:link, .c73 a:visited { color:#737373; }
.c82, .c82 a:link, .c82 a:visited { color:#828282; }
.c88, .c88 a:link, .c88 a:visited { color:#888888; }
.c9c, .c9c a:link, .c9c a:visited { color:#9c9c9c; }
.cae, .cae a:link, .cae a:visited { color:#aeaeae; }
.cbe, .cbe a:link, .cbe a:visited { color:#bebebe; }
.cce, .cce a:link, .cce a:visited { color:#cecece; }
.cdd, .cdd a:link, .cdd a:visited { color:#dddddd; }
.pagetop a:visited { color:#000000;}
.topsel a:link, .topsel a:visited { color:#ffffff; }
.subtext a:link, .subtext a:visited { color:#828282; }
.comhead a:link, .subtext a:visited { color:#828282; }
.hnmore a:link, a:visited { color:#828282; }

/* dark theme */
.dark #pagespace,
.dark .morespace{display:none}
.dark .morelink,
.dark .itemlist,
.dark .fatitem{margin-top:16px}
.dark select,
.dark input,
.dark textarea{background:#000;border-color:#999;color:#fff}
.dark .hnuser font{color:#9c0}
.dark .age{display:inline-block;margin:0 0 4px}
body.dark { background:#000;color:#eee; }
.dark td { background:#333;color:#eee; }
.dark .admin td { color:#eee; }
.dark .subtext td { color:#aaa; }
.dark .default { color:#aaa; }
.dark .admin   { color:#eee; }
.dark .title   { color:#aaa; }
.dark .subtext { color:#aaa; }
.dark .yclinks { color:#aaa; }
.dark .pagetop { color:#ddd; }
.dark .comhead { color:#aaa; }
.dark .c00{color:#ccc}
.dark a:link,
.dark .c00 a:link { color:#adf; }
.dark .pagetop a:link,
.dark .itemlist a:link {color:#ddd}
.dark .pagetop a:visited,
.dark .itemlist a:visited {color:#999}
.dark .c5a, .dark .c5a a:link, .dark .c5a a:visited { color:#bbb; }
.dark .c73, .dark .c73 a:link, .dark .c73 a:visited { color:#aaa; }
.dark .c82, .dark .c82 a:link, .dark .c82 a:visited { color:#999; }
.dark .c88, .dark .c88 a:link, .dark .c88 a:visited { color:#888; }
.dark .c9c, .dark .c9c a:link, .dark .c9c a:visited { color:#777; }
.dark .cae, .dark .cae a:link, .dark .cae a:visited { color:#666; }
.dark .cbe, .dark .cbe a:link, .dark .cbe a:visited { color:#555; }
.dark .cce, .dark .cce a:link, .dark .cce a:visited { color:#444; }
.dark .cdd, .dark .cdd a:link, .dark .cdd a:visited { color:#333; }
.dark .topsel a:link, .dark .topsel a:visited { color:#fff;font-weight:bold }
.dark .subtext a:link, .dark .subtext a:visited,
.dark a:visited,
.dark .hnmore a:link,
.dark a:visited { color:#68b; }
.dark .comhead a:link{color:#c96}
.dark .comhead a:visited{color:#963}

`);
```