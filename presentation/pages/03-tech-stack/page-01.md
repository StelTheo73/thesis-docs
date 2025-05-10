# Tech Stack Selection

<p class='slide-subtitle'>Platform, Framework & Game Engine Selection</p>

<div class='section-wrapper container'>
    <div
      class='image-wrapper item-1-1 grey-shadow bg-white-smoke rounded-md'
      v-click='+1'
      v-motion
      :initial="{ x: -80 }"
      :enter="{ x: 0 }"
    >
      <img src='../../assets/cross_platform.png' width='300'/>
    </div>
    <div
      class='item-1-2'
      v-click='+1'
      v-motion
      :initial="{ x: 80 }"
      :enter="{ x: 0 }"
    >
      <ul class='flex-list'>
        <li>
          We chose to a cross-platform framework and develop an application for Android and iOS to reach a wider audience.
        </li>
        <li>
          Cross-platform frameworks achieve code reusability, which is essential for maintaining a single codebase and offer a consistent user experience across platforms.
        </li>
        <li>
          Cross-platform frameworks offer a balance between performance and development time and cost.
        </li>
      </ul>
    </div>
    <hr class='item-2'/>
    <div
      class='image-wrapper item-3-1 grey-shadow bg-white-smoke rounded-md'
      v-click='+2'
      v-motion
      :initial="{ y: -100 }"
      :enter="{ y: 0 }"
    >
      <img src='../../assets/flutter-black.png' width='200'/>
      <span id="plus-sign">+</span>
      <img src='../../assets/flame.png' width='200'/>
    </div>
    <div
      class='item-3-2'
      v-click='+3'
      v-motion
      :initial="{ x: -100 }"
      :enter="{ x: 0 }"
    >
      <ul class='flex-list'>
        <li>
          Flutter is lighter, faster, produces smaller packages and offers better integration with CI/CD pipelines, compared to other cross-platform frameworks.
        </li>
        <li>
          Flame Game Engine is built on top of Flutter, so we don't have to use a third-party game engine.
        </li>
        <li>
          We found Dart libraries that can be used to simulate quantum circuits.
        </li>
      </ul>
    </div>
</div>

<style>
  .container {
    column-gap: 2rem;
  }

  hr {
    width: 100%;
    margin-top: 1rem;
    margin-bottom: 2rem;
    margin-left: 0;
    margin-right: 0;
  }

  #plus-sign {
    margin-top: 0.5em;
  }

  .image-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 1em;
    height: 180px;
  }

  .item-1-1 {
    grid-row: 1;
    grid-column: 1;
  }

  .item-1-2 {
    grid-row: 1;
    grid-column: 2;
  }

  .item-2 {
    grid-row: 2;
    grid-column: 1 / span 2;
  }

  .item-3-1 {
    grid-row: 3;
    grid-column: 1;
  }

  .item-3-2 {
    grid-row: 3;
    grid-column: 2;
  }
</style>
