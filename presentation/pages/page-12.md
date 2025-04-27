# Application Presentation

<p class='slide-subtitle'>Demo</p>

<div class='section-wrapper'>
  <div>
    <h6>Onboarding</h6>
    <div class='video-wrapper grey-shadow rounded-xl'>
      <SlidevVideo autoplay controls>
        <source
          src='../assets/videos/onboarding.webm'
          type='video/webm'
          class='rounded-xl'
        />
      </SlidevVideo>
    </div>
  </div>
  <div v-click='+1'>
    <h6>Tutorial</h6>
    <div class='video-wrapper grey-shadow rounded-xl'>
      <SlidevVideo v-click autoplay controls>
        <source
          src='../assets/videos/tutorial.webm'
          type='video/webm'
          class='rounded-xl'
        />
      </SlidevVideo>
    </div>
  </div>
  <div v-click='+2'>
    <h6>Gameplay</h6>
    <div class='video-wrapper grey-shadow rounded-xl'>
      <SlidevVideo v-click autoplay controls>
        <source
          src='../assets/videos/gameplay.webm'
          type='video/webm'
          class='rounded-xl'
        />
      </SlidevVideo>
    </div>
  </div>
</div>

<style>
  .section-wrapper {
    position: absolute;
    top: 18%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    column-gap: 2em;
  }

  .video-wrapper {
    max-width: 220px;
  }
</style>
