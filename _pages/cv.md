---
layout: archive
title: "CV (two versions)"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<p>
  <a href="#" id="btn-industry_general" onclick="showCV('industry_general'); return false;"><strong>Industry (general)</strong></a>
  &nbsp;|&nbsp;
  <a href="#" id="btn-academic" onclick="showCV('academic'); return false;">Academic</a>
  
</p>

<iframe id="cv-frame" src="/files/CV_academic.pdf" width="100%" height="750" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>

<p id="cv-download">
  You can download a PDF copy of my CV (updated October 13th 2026)
  <a id="cv-link" href="/files/CV_academic.pdf">here</a>.
</p>

<script>
function showCV(type) {
  var file = '/files/CV_' + type + '.pdf';
  document.getElementById('cv-frame').src = file;
  document.getElementById('cv-link').href = file;
  document.getElementById('btn-academic').innerHTML = type === 'academic' ? '<strong>Academic CV</strong>' : 'Academic';
  document.getElementById('btn-industry_general').innerHTML = type === 'industry_general' ? '<strong>Industry (general)</strong>' : 'Industry (general)';
  history.replaceState(null, '', '#' + type);
}
window.addEventListener('DOMContentLoaded', function () {
  if (location.hash === '#industry_general') showCV('industry_general');
});
</script>