<script>
    export let closePopup;
  </script>
  
  <div class="popup" on:click={closePopup}>
    <div class="popup-content">
      <button class="close-button" on:click={closePopup}>&times;</button>
      <div class="popup-section">
        <h3>Email Marketing</h3>
        <p class="custom-paragraph">Engage talent at the right time, promote your business to the right audience.</p>
      </div>
      <div class="popup-section">
        <h3>Applicant Tracking System</h3>
        <p class="custom-paragraph">Candidate sharing, boolean searches, interview scheduling, automation and more.</p>
      </div>
      <div class="popup-section">
        <h3>Website Integration</h3>
        <p class="custom-paragraph">Turn your WordPress website into a fully featured job-board using our FREE plugins.</p>
      </div>
      <div class="popup-section">
        <h3>Job Distribution</h3>
        <p class="custom-paragraph">Get your job in front of millions of candidates, manage applicants in one place.</p>
      </div>
      <div class="popup-section">
        <h3>Search & Import</h3>
        <p class="custom-paragraph">Search and import candidates from CV-Library and TotalJobs with just a few clicks.</p>
      </div>
      <div class="popup-section">
        <h3>Recruiting Automation</h3>
        <p class="custom-paragraph">Boost your team's productivity by creating workflows that automate repetitive and common tasks.</p>
      </div>
    </div>
  </div>
  