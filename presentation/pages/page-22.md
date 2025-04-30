# Conclusions

<p class='slide-subtitle'>Key Findings</p>

<div class='section-wrapper'>
  <div class='text-wrapper grey-shadow rounded-md'>
    <ul class='flex-list none'>
      <li class='check'>
        The game is an effective learning tool and successfully introduces quantum computing concepts.
      </li>
      <li class='check'>
        The average time to complete the game was 18 minutes, making the game suitable to be used as an educational tool during a university lecture.
      </li>
    </ul>
  </div>
  <div
    class='text-wrapper grey-shadow rounded-md'
    v-click='+1'
    v-motion
    :initial="{ y: -80 }"
    :enter="{ y: 0 }"
  >
    <ul class='flex-list none'>
      <li class='check'>
        The game is suitable for users with no prior experience in the field.
      </li>
      <li class='check'>
        The incentive system was effective, enhancing motivation.
      </li>
      <li class='check'>
        The game has a positive impact on information retention.
      </li>
    </ul>
  </div>
  <div
    class='text-wrapper grey-shadow rounded-md'
    v-click='+2'
    v-motion
    :initial="{ y: -80 }"
    :enter="{ y: 0 }"
  >
    <ul class='flex-list none'>
      <li class='warn'>
        The game should be extended with more challenging puzzles.
      </li>
      <li class='warn'>
        Sound effects and background music should be added to enhance immersion.
      </li>
      <li class='warn'>
        More information about superposition should be provided.
      </li>
    </ul>
  </div>
</div>

<style>
  .section-wrapper {
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
    max-width: 300px;
    padding: 1em;
  }
</style>
