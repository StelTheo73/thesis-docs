# Evaluation

<p class='slide-subtitle'>Focus Group Results</p>

<div class='section-wrapper'>
  <p>Focus group results align closely with questionnaire results, confirming the game's strengths and weaknesses.</p>

  <div class='results-wrapper'>
    <div
      class='grey-shadow rounded-md fade-out-vclick hide-before-click-vclick'
      v-click='+1'
    >
      <ul class='text-wrapper none'>
        <h2>Strengths</h2>
        <li class='check'>
          Simple mechanics.
        </li>
        <li class='check'>
          Effective incentive system.
        </li>
        <li class='check'>
          Suitable for users with no prior knowledge.
        </li>
        <li class='check'>
          Predictable navigation.
        </li>
      </ul>
    </div>
    <div
      class='grey-shadow rounded-md'
      v-click='+2'
    >
      <ul class='text-wrapper none'>
        <h2>Weak Spots</h2>
        <li class='warn'>
          Low immersion due to lack of background music and sound effects.
        </li>
        <li class='warn'>
          Lack of challenging puzzles.
        </li>
        <li class='warn'>
          More information about superposition.
        </li>
        <li class='warn'>
          Hints for difficult puzzles.
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
    height: 350px;
    width: 450px;
    padding: 1em;
  }

  .text-wrapper h2 {
    margin-bottom: 1em;
  }

  ul li {
    margin-bottom: 1em;
  }
</style>
