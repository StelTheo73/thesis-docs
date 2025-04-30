# Evaluation

<p class='slide-subtitle'>GUESS-18 Questionnaire results</p>

<div class='section-wrapper'>

  <div
    class='text-wrapper grey-shadow rounded-md'
    v-click='+1'
    v-motion
    :initial="{ x: +80 }"
    :enter="{ x: 0 }"
  >
    <ul class='flex-list none'>
      <h2>Strengths</h2>
      <li class='check'>
        <strong>Visual Aesthetics (6.4) & Enjoyment (6.2):</strong> enjoyable and visually appealing.
      </li>
      <li class='check'>
        <strong>Usability (6):</strong> ease of use and navigation.
      </li>
      <li class='check'>
        <strong>Personal Gratification (~6) & Creative Freedom (5.4):</strong> sense of accomplishment and creativity.
      </li>
    </ul>
  </div>
  <div class='img-wrapper grey-shadow rounded-md'>
    <img src='../assets/images/evaluation/guess.png' class='rounded-md'/>
  </div>
  <div
    class='text-wrapper grey-shadow rounded-md'
    v-click='+1'
    v-motion
    :initial="{ x: -80 }"
    :enter="{ x: 0 }"
  >
    <ul class='flex-list none'>
      <h2>Weak Spots</h2>
      <li class='warn'>
        <strong>Narratives (5.3):</strong> storytelling is good, but could be improved.
      </li>
      <!-- I placed narratives at weak spots because some players asked for more information, especially regarding superposition -->
      <li class='warn'>
        <strong>Player Engrossment (3.9):</strong> players were not fully focused on the game.
      </li>
      <li class='warn'>
        <strong>Social Connectivity (3.9) & Audio Aesthetics (1):</strong> expected, since the game is single-player and has no audio.
      </li>
    </ul>
  </div>
</div>

<style>
  .section-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    column-gap: 20px;
  }

  .img-wrapper {
    max-width: 600px;
    height: 350px;
    display: flex;
    justify-content: center;
  }

  .text-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    max-height: 350px;
    max-width: 350px;
    padding: 1em;
  }
</style>
