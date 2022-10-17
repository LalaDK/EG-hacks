# EG-hacks

## Talentsoft autoclicker
Open console (F12) and paste code:
```javascript
let selectors = [
  'img[src*=btn_suite_roll.png]',
  '.next-lesson a'
];
setInterval(() => {
  var frame = document
    .getElementById("launch_wrapper_content").contentDocument
    .getElementById("sco_frame").contentDocument
    .getElementById("content-frame").contentDocument;

  if (frame) {
    let page = frame.getElementById("page-wrap");
    if (page) {
      page.scrollTop = 9999;
      selectors.forEach((selector) => {
        let el = frame.querySelector(selector);
        if (el) {
          el.click();
        }
      });
      
    }
  }
}, 400);
```
