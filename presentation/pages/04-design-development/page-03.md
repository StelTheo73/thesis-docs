# Design and Development Process

<p class='slide-subtitle'>Conceptual Design (2/2)</p>

<div class='section-wrapper'>
  <ol class='ol-flex' start=2>
    <li>
      <p><strong>Mechanics:</strong> Genre and Mechanics Definition</p>
      <ul>
        <li>2D Game, combination of Puzzle and Shooter Genres</li>
        <li v-click>The spaceship that can move horizontally across the screen, between discrete positions</li>
        <li v-click='+2'>The position of the spaceship is determined by the state of the quantum register</li>
        <li v-click='+2'>The state of the quantum register -and therefore the position of the spaceship- can be altered by applying quantum gates</li>
        <li v-click='+3'>The player can launch missiles by pressing a button</li>
        <li v-click='+3'>Implementation of motion equations to determine the trajectory of the missiles</li>
        <li v-click='+4'>Collision detection: Flame Game Engine provides a built-in collision detection system</li>
      </ul>
    </li>
    <li
      v-click='+5'
      v-motion
      :initial="{ y: -80 }"
      :enter="{ y: 0 }"
    >
      <p><strong>Narratives & Aesthetics:</strong> GBL Elements Selection</p>
      <ul>
        <li v-click='+5'>Narratives via overlays to introduce theory and game rules</li>
        <li v-click='+5'>Graceful failure approach allowing mistakes without immediate penalty</li>
        <li v-click='+6'>Incentive System: awarding 1 to 3 stars based on performance (number of gates and missiles used)</li>
        <li v-click='+6'>Incentive System: Unlocking new spaceships to boost motivation and engagement</li>
        <li v-click='+6'>Incentive System: No leaderboard to prevent frustration or discrimination among players (Dominguez et all. 2013) <Link to=''>[2]</Link></li>
      </ul>
    </li>
  </ol>
</div>

<style>
  ol.ol-flex li{
    width: 90%;
  }

  ol > li > p {
    font-size: larger;
    text-decoration: underline;
  }
</style>
