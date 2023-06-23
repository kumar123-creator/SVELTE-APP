<script>
	import { createEventDispatcher } from 'svelte';
	import 'bootstrap/dist/css/bootstrap.min.css';
	
	import OverviewPopup from './OverviewPopup.svelte';
	import WhyRecruitlyPopup from './WhyRecruitlyPopup.svelte';
	import PricingPopup from './PricingPopup.svelte';
	import AutomationPopup from './AutomationPopup.svelte';
	
	const dispatch = createEventDispatcher();
	let activePopup = null;
	let featureIndex = 0;
	const features = [
	  { text: 'ATS', color: 'black' },
	  { text: 'CRM', color: 'black' },
	  { text: 'Marketing', color: 'black' }
	];
  
	function openPopup(popup) {
	  activePopup = popup;
	}
  
	function closePopup() {
	  activePopup = null;
	}
  
	function nextFeature() {
	  featureIndex = (featureIndex + 1) % features.length;
	}
  
	setInterval(nextFeature, 2000);
  </script>
  
  <main>
	<div class="container">
	  <h1 class="display-4" style="color: blue; font-weight: 700;">Recruitment</h1>
	  <h1 class="display-4" style="color: blue; font-weight: 700;">
		<span class="feature-text" style="color: {features[featureIndex].color}; font-weight: 700;">
		  {features[featureIndex].text}
		</span>
		System
	  </h1>
	  <p class="card-text">Recruitly® is built to streamline agency recruitment processes and help businesses grow as a result.</p>
	</div>
	<div class="overview-button-container">
	  <button class="overview-button" on:click={() => openPopup('overview')}>Overview</button>
	</div>
  </main>
  
  <div class="information">
	<p on:click={() => openPopup('whyRecruitly')} style="color: blue;">Why Recruitly</p>
	<p on:click={() => openPopup('automation')} style="color: blue;">Automation</p>
	<p on:click={() => openPopup('pricing')} style="color: blue;">Pricing</p>
  </div>
  
  {#if activePopup === 'whyRecruitly'}
	<WhyRecruitlyPopup on:closePopup={closePopup} />
  {/if}
  
  {#if activePopup === 'pricing'}
	<PricingPopup on:closePopup={closePopup} />
  {/if}
  
  {#if activePopup === 'overview'}
	<OverviewPopup on:closePopup={closePopup} />
  {/if}
  
  {#if activePopup === 'automation'}
	<AutomationPopup on:closePopup={closePopup} />
  {/if}
  
  <style>
	/* Add custom styles for your opening page here */
	.container {
	  text-align: center;
	  margin-top: 200px;
	}
	h1.display-4 {
	  font-size: 3.5rem;
	  margin-bottom: 0.5rem;
	  font-stretch: expanded;
	}
	.font-weight-bold {
	  font-weight: bold;
	}
  
	.header {
	  background-color: #f8f9fa;
	  padding: 20px;
	  text-align: center;
	}
  
	.information {
	  position: absolute;
	  top: 50px;
	  right: 270px;
	  display: flex;
	  flex-direction: row;
	  align-items: center;
	}
  
	.information p {
	  margin: 0;
	  margin-left: 10px;
	  cursor: pointer;
	}
  
	.popup {
	  position: fixed;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 100%;
	  background-color: rgba(0, 0, 0, 0.5);
	  display: flex;
	  justify-content: center;
	  align-items: center;
	}
  
	.popup-content {
	  position: relative;
	  background-color: #fff;
	  padding: 20px;
	  text-align: center;
	  border-radius: 5px;
	  width: 80%;
	  height: 80%;
	  max-width: 800px;
	  display: flex;
	  flex-wrap: wrap;
	  justify-content: center;
	  align-items: center;
	  overflow-y: auto;
	}
  
	.popup-section {
	  width: calc(50% - 20px);
	  height: 25%;
	  padding: 10px;
	}
  
	.custom-paragraph {
	  text-align: center;
	}
  
	.popup-content h3 {
	  text-align: center;
	  color: blue;
	}
  
	.popup-content p.custom-paragraph {
	  width: 100%;
	  text-align: center;
	}
  
	body {
	  background-color: #e2f3fc;
	}
	.close-button {
	  position: absolute;
	  top: 0px;
	  right: 1px;
	  font-size: 24px;
	  color: #f00f22;
	  background: transparent;
	  border: none;
	  cursor: pointer;
	}
	.overview-button {
	  margin-top: 10px;
	  padding: 10px 20px;
	  background-color:blueviolet;
	  color: black;
	  border: none;
	  border-radius: 5px;
	  font-size: 16px;
	  cursor: pointer;
	  display: flex;
	  align-items: center;
	  margin: 0 auto;
	}
	.popup-video-section {
	  width: 100%;
	  text-align: center;
	}
  
	.popup-video {
	  width: 100%;
	  height: 400px;
	}  
  </style>
  