# EG-hacks

## Talentsoft autoclicker
Open console (F12) and paste code:
```
setInterval(() => {
  var frame = document
    .getElementById("launch_wrapper_content").contentDocument
    .getElementById("sco_frame").contentDocument
    .getElementById("content-frame").contentDocument;

  if (frame) {
    let page = frame.getElementById("page-wrap");
    if (page) {
      page.scrollTop = 9999;
      let el = frame.querySelector(".next-lesson a");
      if (el) {
        el.click();
      } else {
        console.info("No next-lession element")
      }
    } else {
      console.info("No page element")
    }
  }
}, 400);
```
