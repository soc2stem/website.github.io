<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Contact</title>
  <link rel="stylesheet" href="css/style.css" />
  <script src="js/config.js"></script>
</head>
<body>

  <header id="site-header"></header>

  <div class="page-hero">
    <h1>Contact Us</h1>
    <p>Reach out for collaborations, inquiries, or joining the lab.</p>
  </div>

  <div style="background:#fff;">
    <div class="section">
      <div class="contact-grid">

        <div class="contact-info">
          <h2 class="section-title">Get in Touch</h2>
          <p id="contact-intro">We welcome inquiries from prospective students, collaborators, and the press.</p>

          <p style="margin-top:24px;">
            <strong>Email</strong><br>
            <a id="contact-email" href="#"></a>
          </p>
          <p>
            <strong>Address</strong><br>
            <span id="contact-address"></span>
          </p>
          <p>
            <strong>Department</strong><br>
            <span id="contact-dept"></span><br>
            <span id="contact-uni"></span>
          </p>

          <div style="margin-top:28px; display:flex; gap:10px; flex-wrap:wrap;" id="social-links"></div>
        </div>

        <div style="display:flex; flex-direction:column; gap:20px;">
          <div class="contact-block">
            <h3>🎓 Prospective PhD Students</h3>
            <!-- ✏️ EDIT: Update this with your actual admissions info -->
            <ul class="joining-list">
              <li>Applications are handled through the <a href="#">department admissions portal</a>.</li>
              <li>We recruit students with backgrounds in CS, math, statistics, or related fields.</li>
              <li>Email the PI with your CV and a brief research statement if interested.</li>
              <li>Mention specific papers from our group you found interesting.</li>
            </ul>
          </div>

          <div class="contact-block">
            <h3>🤝 Collaborations</h3>
            <!-- ✏️ EDIT: Adjust collaboration preferences -->
            <ul class="joining-list">
              <li>We actively seek academic and industry collaborators.</li>
              <li>Email us with a brief description of your project or shared interests.</li>
              <li>We are open to co-advising students across institutions.</li>
            </ul>
          </div>

          <div class="contact-block">
            <h3>📍 Finding Us</h3>
            <!-- ✏️ EDIT: Add building/room info -->
            <p style="font-size:.93rem; color:#5A5A5A;">
              We are located in the <strong>Gates Dell Complex (GDC)</strong> on the UT Austin main campus.
              Visitor parking is available in nearby garages. See the
              <a href="https://www.utexas.edu/maps/" target="_blank">UT Austin campus map</a> for directions.
            </p>
          </div>
        </div>

      </div>
    </div>
  </div>

  <footer id="site-footer"></footer>

  <script src="js/site.js"></script>
  <script>
    const c = LAB_CONFIG;
    document.title = `Contact — ${c.labName}`;

    const emailEl = document.getElementById('contact-email');
    emailEl.href = `mailto:${c.email}`;
    emailEl.textContent = c.email;

    document.getElementById('contact-address').textContent = c.address;
    document.getElementById('contact-dept').textContent = c.department;
    document.getElementById('contact-uni').textContent = c.university;

    const socials = document.getElementById('social-links');
    if (c.twitterHandle) socials.innerHTML += `<a class="btn btn-orange" href="https://twitter.com/${c.twitterHandle.replace('@','')}" target="_blank" style="font-size:.82rem; padding:8px 16px;">Twitter/X</a>`;
    if (c.githubOrg)     socials.innerHTML += `<a class="btn btn-orange" href="https://${c.githubOrg}" target="_blank" style="font-size:.82rem; padding:8px 16px;">GitHub</a>`;
    if (c.googleScholar) socials.innerHTML += `<a class="btn btn-orange" href="${c.googleScholar}" target="_blank" style="font-size:.82rem; padding:8px 16px;">Google Scholar</a>`;
  </script>
</body>
</html>
