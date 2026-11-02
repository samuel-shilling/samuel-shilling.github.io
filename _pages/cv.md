---
layout: archive
title: "CV (two versions)"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<p>
  <a href="#" id="btn-industry_general" onclick="showCV('Q_sprs'); return false;"><strong>Quantitative Research</strong></a>
  &nbsp;|&nbsp;
  <a href="#" id="btn-data_science" onclick="showCV('DS_sprs'); return false;">Data Science</a>
</p>

<iframe id="cv-frame" src="/files/CV_Q_sprs.pdf" width="100%" height="750" frameborder="no" border="0" marginwidth="0" marginheight="0"></iframe>

<p id="cv-download">
  You can download a PDF copy of my CV (updated October 28th 2026)
  <a id="cv-link" href="/files/CV_Q_sprs.pdf" target="_blank" rel="noopener">here</a>
</p>

<script>
function showCV(type) {
  var file = '/files/CV_' + type + '.pdf';
  document.getElementById('cv-frame').src = file;
  document.getElementById('cv-link').href = file;
  document.getElementById('btn-data_science').innerHTML = type === 'DS_sprs' ? '<strong>Data Science</strong>' : 'Data Science';
  document.getElementById('btn-industry_general').innerHTML = type === 'Q_sprs' ? '<strong>Quantitative Research</strong>' : 'Quantitative Research';
  history.replaceState(null, '', '#' + type);
}
window.addEventListener('DOMContentLoaded', function () {
  if (location.hash === '#DS_sprs') showCV('DS_sprs');
});
</script>