---
layout: default
title: "Privacy Policy"
permalink: /privacy/
---

<style>
  .privacy-wrapper { max-width: 820px; margin: 0 auto; padding: 20px 0; }
  .privacy-hero {
    background: linear-gradient(135deg, #1e3c72, #2a5298, #059669);
    border-radius: 16px; padding: 38px 35px; color: white; margin-bottom: 35px;
  }
  .privacy-hero h1 { font-size: 2rem; font-weight: 800; color: white; margin: 0 0 8px; }
  .privacy-hero p  { opacity: 0.88; margin: 0; font-size: 0.9rem; }
  .privacy-section {
    background: white; border-radius: 13px; padding: 26px 30px;
    margin-bottom: 18px; border-left: 5px solid #1e3c72;
    box-shadow: 0 4px 14px rgba(0,0,0,0.05);
  }
  .privacy-section h2 {
    font-size: 1.05rem; font-weight: 800; color: #1e3c72;
    margin: 0 0 12px; display: flex; align-items: center; gap: 10px;
  }
  .privacy-section p, .privacy-section ul { color: #555; line-height: 1.75; margin: 0; font-size: 0.93rem; }
  .privacy-section ul { padding-left: 20px; }
  .privacy-section ul li { margin-bottom: 6px; }
  .data-table { width: 100%; border-collapse: collapse; margin-top: 14px; font-size: 0.88rem; border-radius: 10px; overflow: hidden; }
  .data-table th { background: #1e3c72; color: white; padding: 11px 14px; text-align: left; }
  .data-table td { padding: 10px 14px; border-bottom: 1px solid #e5e7eb; color: #444; }
  .data-table tr:nth-child(even) td { background: #f8faff; }
  .data-table tr:last-child td { border-bottom: none; }
  .rights-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 14px; }
  .right-item {
    background: #eff6ff; border: 1px solid #bfdbfe; border-radius: 10px;
    padding: 12px 14px; font-size: 0.86rem; color: #1e40af;
    display: flex; align-items: flex-start; gap: 8px;
  }
  .right-item i { margin-top: 2px; flex-shrink: 0; }
  @media (max-width: 600px) { .rights-grid { grid-template-columns: 1fr; } }
</style>

<div class="privacy-wrapper">

  <div class="privacy-hero">
    <h1><i class="fas fa-shield-alt"></i> Privacy Policy</h1>
    <p><strong>Effective Date: March 15, 2026</strong> &nbsp;|&nbsp; Last Updated: {{ site.time | date: "%B %d, %Y" }}</p>
    <p style="margin-top:8px;">
      This Privacy Policy explains how drpraveendra.github.io collects, uses, and protects
      information when you visit this website. We are committed to protecting your privacy.
    </p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-info-circle"></i> 1. Who We Are</h2>
    <p>This website is operated by <strong>Dr. Praveendra Singh</strong>, Assistant Professor of Mathematics,
    Government College Kherwara, Udaipur, Rajasthan, India.
    Contact: <a href="mailto:drpraveendra.singh@gmail.com" style="color:#1e3c72;">drpraveendra.singh@gmail.com</a></p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-database"></i> 2. What Data is Collected</h2>
    <p>This website does <strong>not</strong> directly collect personal data. However, third-party services used on this site may collect the following:</p>
    <table class="data-table">
      <thead><tr><th>Data Type</th><th>Collected By</th><th>Purpose</th></tr></thead>
      <tbody>
        <tr><td>IP address</td><td>GitHub Pages (hosting)</td><td>Server logs, security</td></tr>
        <tr><td>Browser type, OS</td><td>GitHub Pages</td><td>Technical analytics</td></tr>
        <tr><td>Pages visited, time spent</td><td>Google Search Console</td><td>SEO performance tracking</td></tr>
        <tr><td>Ad interaction data</td><td>Google AdSense (future)</td><td>Serving relevant ads</td></tr>
        <tr><td>GitHub username</td><td>Giscus (comments)</td><td>Comment authentication</td></tr>
        <tr><td>Cookies</td><td>Google, GitHub</td><td>Session management, ads</td></tr>
      </tbody>
    </table>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-cookie-bite"></i> 3. Cookies</h2>
    <p>This website uses cookies from third-party services:</p>
    <ul>
      <li><strong>GitHub Pages:</strong> Session and security cookies for hosting</li>
      <li><strong>Google AdSense (future):</strong> DART cookies to serve personalised ads based on browsing history</li>
      <li><strong>Giscus:</strong> GitHub authentication cookies for the comment system</li>
    </ul>
    <p style="margin-top:10px;">You can disable cookies in your browser settings at any time. You may also opt out of personalised Google ads at
    <a href="https://www.google.com/settings/ads" target="_blank" rel="noopener" style="color:#1e3c72;">Google Ads Settings</a>.</p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-ad"></i> 4. Google AdSense & Advertising</h2>
    <p>This website participates in (or plans to participate in) the Google AdSense programme. Google uses cookies to serve ads based on your prior visits to this and other websites. These ads help support the free educational content on this site.</p>
    <ul>
      <li>Google's use of cookies enables personalised advertising</li>
      <li>You can opt out at <a href="https://www.google.com/settings/ads" target="_blank" rel="noopener" style="color:#1e3c72;">Google Ads Settings</a></li>
      <li>We do not control which specific ads are shown</li>
      <li>We do not share your personal data with advertisers</li>
    </ul>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-comments"></i> 5. Comments (Giscus)</h2>
    <p>This website uses <strong>Giscus</strong> for blog post comments, which is powered by GitHub Discussions.
    To leave a comment, you need a GitHub account. Your GitHub username and comment are stored on GitHub's servers
    under their <a href="https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement" target="_blank" rel="noopener" style="color:#1e3c72;">Privacy Policy</a>.
    We do not store comment data independently.</p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-external-link-alt"></i> 6. Third-Party Links</h2>
    <p>This website contains links to external platforms including YouTube, Telegram, Google Scholar, ResearchGate, and Amazon.
    These sites have their own privacy policies. We are not responsible for the privacy practices of any third-party website.
    We encourage you to read the privacy policy of any external site you visit.</p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-user-check"></i> 7. Your Rights</h2>
    <div class="rights-grid">
      <div class="right-item"><i class="fas fa-eye"></i> Right to know what data is collected about you</div>
      <div class="right-item"><i class="fas fa-trash"></i> Right to request deletion of your data</div>
      <div class="right-item"><i class="fas fa-ban"></i> Right to opt out of personalised advertising</div>
      <div class="right-item"><i class="fas fa-file-export"></i> Right to data portability where applicable</div>
      <div class="right-item"><i class="fas fa-edit"></i> Right to correct inaccurate information</div>
      <div class="right-item"><i class="fas fa-hand-paper"></i> Right to object to certain processing</div>
    </div>
    <p style="margin-top:14px;">To exercise any of these rights, contact us at <a href="mailto:drpraveendra.singh@gmail.com" style="color:#1e3c72;font-weight:700;">drpraveendra.singh@gmail.com</a>.</p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-child"></i> 8. Children's Privacy</h2>
    <p>This website is intended for students aged 18 and above. We do not knowingly collect personal information from children under 13. If you believe a child has provided personal information, please contact us immediately.</p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-sync-alt"></i> 9. Changes to This Policy</h2>
    <p>We may update this Privacy Policy from time to time. The "Last Updated" date at the top of this page will reflect any changes. Continued use of the website after changes constitutes acceptance of the revised policy.</p>
  </div>

  <div class="privacy-section">
    <h2><i class="fas fa-envelope"></i> 10. Contact</h2>
    <p>For any privacy-related questions or concerns, please contact:<br>
    <strong>Dr. Praveendra Singh</strong><br>
    Government College Kherwara, Udaipur, Rajasthan, India<br>
    Email: <a href="mailto:drpraveendra.singh@gmail.com" style="color:#1e3c72;font-weight:700;">drpraveendra.singh@gmail.com</a></p>
  </div>

</div>
