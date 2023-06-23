<script>
    export let closePopup;
  </script>
  
  <div class="popup pricing-popup">
    <div class="popup-content">
      <button class="close-button" on:click={closePopup}>&times;</button>
      <div class="popup-section">
        <h3>Recruitly Pricing</h3>
        <div class="pricing-tier">
          <h4>Solo</h4>
          <p class="custom-paragraph">For independent recruiters</p>
          <p class="custom-paragraph pricing-details">
            $35/user/month
          </p>
        </div>
        <div class="pricing-tier">
          <h4>Startup</h4>
          <p class="custom-paragraph">For startup agencies</p>
          <p class="custom-paragraph pricing-details">
            $50/user/month
          </p>
        </div>
        <div class="pricing-tier">
          <h4>Professional</h4>
          <p class="custom-paragraph">For established teams</p>
          <p class="custom-paragraph pricing-details">
            $75/user/month
          </p>
        </div>
        <div class="pricing-tier">
          <h4>Enterprise</h4>
          <p class="custom-paragraph">For large organizations</p>
          <p class="custom-paragraph pricing-details">
            $100/user/month
          </p>
        </div>
      </div>
    </div>
  </div>
  