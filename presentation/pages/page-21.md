# Evaluation

<p class='slide-subtitle'>Focus Group results</p>

<div class='section-wrapper'>
  <p>Focus group results align closely with questionnaire results, confirming the game's strengths and weaknesses.</p>

  <div class='results-wrapper'>
    <div
      class='grey-shadow rounded-md'
      v-click='+1'
      v-motion
      :initial="{ y: -80 }"
      :enter="{ y: 0 }"
    >
      <ul class='text-wrapper none'>
        <h2>Strengths</h2>
        <li class='check'>
          Simple mechanics that helped players focus on the game.
        </li>
        <li class='check'>
          Effective incentive system, enhanced motivation and engagement.
        </li>
        <li class='check'>
          Suitable for users with no prior experience in the field.
        </li>
        <li class='check'>
          Clear and predictable navigation.
        </li>
      </ul>
    </div>
    <div
      class='grey-shadow rounded-md'
      v-click='+2'
      v-motion
      :initial="{ y: -80 }"
      :enter="{ y: 0 }"
    >
      <ul class='text-wrapper none'>
        <h2>Weak Spots</h2>
        <li class='warn'>
          Low immersion due to lack of background music and sound effects.
        </li>
        <li class='warn'>
          Some players found the game too easy and suggested adding more challenging puzzles.
        </li>
        <li class='warn'>
          Some players requested more explanation around the concept of superposition.
        </li>
        <li class='warn'>
          Hints for difficult puzzles were suggested.
        </li>
      </ul>
    </div>
  </div>
</div>

<style>
  .section-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    height: 65%;
  }

  .section-wrapper .results-wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
  }

  .text-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: max-content;
    max-width: 400px;
    padding: 1em;
  }

  .text-wrapper h2 {
    margin-bottom: 0.5em;
  }
</style>
