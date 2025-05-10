# Application Presentation

<p class='slide-subtitle'>Name, Objective and Main Elements</p>

<div class='section-wrapper'>
  <div class='text-wrapper'>
    <div class='section-1'>
      <p>
        The application we developed is called <em><strong>Qubity</strong></em>.
      </p>
      <p>
        Qubity is inspired by the arcade video-game <em>Space Invaders</em>.
      </p>
      <p>
        The game is a 2D puzzle and shooter game, where the player controls a spaceship that can move horizontally across the screen and shoot missiles upwards.
      </p>
      <p>
        The objective of each level is to destroy all the asteroids on the screen.
      </p>
    </div>
    <hr class='divider' v-click='+1'/>
    <div
      class='section-2'
      v-click='+1'
      v-motion
      :initial="{ y: -80 }"
      :enter="{ y: 0 }"
    >
      <p>
        The game has 30 levels, each level has a different number of asteroids and different gates available.
      </p>
    </div>
    <hr class='divider' v-click='+1'/>
    <div
      class='section-3'
      v-click='+2'
      v-motion
      :initial="{ y: -80 }"
      :enter="{ y: 0 }"
    >
      <p>
        The player has to solve the puzzle by applying the correct gates to the register, in order to move the spaceship to the correct position and then shoot the missiles to destroy the asteroids.
      </p>
    </div>
  </div>
  <div class='image-wrapper grey-shadow rounded-xl'>
    <img src='../../assets/level-30.png' class='rounded-xl'/>
  </div>
</div>

<style>
  .section-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: center;
    column-gap: 2em;
  }

  .text-wrapper {
    padding: 0.5em;
    height: max-content;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .image-wrapper {
    height: max-content;
  }

  .image-wrapper img {
    height: 480px;
    width: 390px;
  }
</style>
