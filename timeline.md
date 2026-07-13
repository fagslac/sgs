---
title: Timeline
---

# Timeline

This will be a timeline displaying all read chapters at their timestamp, with a thread linking them. 
For now it's just the list of chapters:

<ul id="list"></ul>

---

[← Back](index.md)

<script>
var chapters = [{"title": "0 - Prologue", "href": "A0_0/0_0.html"}, {"title": "The POSTMan Show S00E00", "href": "A1_PMS0/pms0.html"}, {"title": "1 - Awakening at Number One, London", "href": "A2_SGS1/sgs1.html"}, {"title": "The POSTMan Show S00E01", "href": "A3_PMS1/pms1.html"}, {"title": "2 - Breakfast at Athena's", "href": "A4_SGS2/sgs2.html"}, {"title": "The POSTMan Show S00E02", "href": "A5_PMS2/pms2.html"}, {"title": "3 - The Royal Cock Pit", "href": "A6_SGS3/sgs3.html"}, {"title": "The POSTMan Show S00E03", "href": "A7_PMS3/pms3.html"}];

var html = '';
for (var i = chapters.length - 1; i >= 0; i--) {
  if (localStorage.getItem(chapters[i].href.replace(/\.html$/, ''))) {
    html += '<li><a href="' + chapters[i].href + '">' + chapters[i].title + '</a></li>';
  }
}
document.getElementById('list').innerHTML = html || '<li style="color:#999">No chapters visited yet.</li>';
</script>
