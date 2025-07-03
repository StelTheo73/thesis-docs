# Literature Review
<p class='slide-subtitle'>Findings (3/3)</p>

<div class='section-wrapper'>
  <div class='text-wrapper'>
    <h2>GBL Elements</h2>
    <ul class='flex-list'>
      <li v-after class='fade-out-vclick'>
        <strong>Learning Mechanics</strong>: Link quantum computing concepts to game mechanics.
      </li>
      <li v-after class='fade-out-vclick'>
        <strong>Assessment Mechanics</strong>: Quiz integration to measure learning outcomes.
      </li>
      <li v-click='+1' class='fade-out-vclick'>
        <strong>Narratives</strong>: Overlays to introduce theory and game rules.
      </li>
      <li v-click='+2' class='fade-out-vclick'>
        <strong>Graceful Failure</strong>: Allowing mistakes without immediate penalty or negative feedback.
      </li>
      <li v-click='+3' class='fade-out-vclick'>
        <strong>Incentive System</strong>: Awarding 1 to 3 stars based on performance.
      </li>
      <li v-click='+3' class='fade-out-vclick'>
        <strong>Incentive System</strong>: Unlocking new spaceships to boost motivation and engagement.
      </li>
      <li v-click='+3' class='fade-out-vclick'>
        <strong>Incentive System</strong>: No leaderboard to prevent frustration and discrimination.
        <Link class='ref-link' to='20'>[2]</Link>
      </li>
    </ul>
  </div>
  <div class='img-group'>
    <div class='img-caption-wrapper' v-click='+1'>
      <div class='image-wrapper grey-shadow bg-white-smoke rounded-xl'>
        <img class='rounded-xl' src='../../assets/images/design/theory_slide.jpg'/>
      </div>
      <span>Figure 2: Narratives.</span>
    </div>
    <div class='img-caption-wrapper' v-click='+3'>
      <div class='image-wrapper grey-shadow bg-white-smoke rounded-xl'>
        <img class='rounded-xl' src='../../assets/images/design/score_and_reward.jpg'/>
      </div>
      <span>Figure 3: Incentive System.</span>
    </div>
  </div>
</div>

<style>
  h2 {
    text-decoration: underline;
    margin-bottom: 1em;
  }

  .section-wrapper {
    position: absolute;
    top: 20%;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
  }

  .image-wrapper img {
    max-width: 220px;
  }

  .img-group {
    display: flex;
    min-height: 500px;
    width: 220px;
  }

  .img-group .img-caption-wrapper.slidev-vclick-prior {
    display: none;
  }

</style>