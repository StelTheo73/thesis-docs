# Application Presentation

<p class='slide-subtitle'>Name, Overview and Demo</p>

<div class='section-wrapper'>
  <div class='text-wrapper grey-shadow rounded-md'>
    <p>
      <strong>Name</strong>: <em>Qubity</em>.
    </p>
    <p>
      <strong>Genre</strong>: Combination, Puzzle and Shooter game.
    </p>
    <p>
      <strong>Main Objective</strong>: Destroy the asteroids.
    </p>
  </div>
  <div class='video-wrapper grey-shadow rounded-xl' v-click='+1'>
    <SlidevVideo v-click autoplay controls class='rounded-xl'>
      <source
        src='../../assets/videos/gameplay.webm'
        type='video/webm'
        class='rounded-xl'
      />
    </SlidevVideo>
  </div>
</div>

<style>
  .section-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    column-gap: 2em;
  }

  .text-wrapper {
    padding: 1em;
    height: max-content;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .video-wrapper {
    max-width: 220px;
  }
</style>
