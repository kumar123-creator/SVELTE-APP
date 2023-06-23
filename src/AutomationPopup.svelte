<script>
    export let closePopup;
  </script>
  
  <div class="popup automation-popup" on:click={closePopup}>
    <div class="popup-content">
      <button class="close-button" on:click={closePopup}>&times;</button>
      <div class="popup-section">
        <h3>Recruiting Automation</h3>
        <p class="custom-paragraph">Increase efficiency by creating workflows that automate repetitive and common tasks, save hours each day.</p>
      </div>
      <div class="popup-section">
        <h3>Save time</h3>
        <p class="custom-paragraph">Increase efficiency by creating workflows that automate repetitive and common tasks, save hours each week.</p>
      </div>
      <div class="popup-section">
        <h3>Be in control</h3>
        <p class="custom-paragraph">Ensure that recruiting standards are enforced automatically, and build a streamlined and error-proof workflow.</p>
      </div>
      <div class="popup-section">
        <h3>Automate everything</h3>
        <p class="custom-paragraph">Create workflows that automate every step of your recruitment process, from initial screening to job offer management.</p>
      </div>
    </div>
  </div>
  