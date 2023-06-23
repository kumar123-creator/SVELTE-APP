<script>
    export let closePopup;
  </script>
  
  <div class="popup" on:click={closePopup}>
    <div class="popup-content">
      <button class="close-button" on:click={closePopup}>&times;</button>
      <div class="popup-video-section">
        <iframe class="popup-video" src="https://www.youtube.com/embed/9L0fVJb7zSk" frameborder="0" allowfullscreen></iframe>
      </div>
    </div>
  </div>
  