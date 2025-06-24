# Conclusions

<p class='slide-subtitle'>Key Findings & Future Work</p>

<div class='section-wrapper'>
  <div class='text-wrapper grey-shadow rounded-md'>
    <ul class='flex-list none'>
      <li class='check'>
        Effective learning tool.
      </li>
      <li class='check'>
        Average completion time: 18 minutes.
      </li>
      <li class='check'>
        Suitable for users with no prior experience in the field.
      </li>
      <li class='check'>
        Effective incentive system, enhances motivation and engagement.
      </li>
      <li class='check'>
        Positive impact on knowledge retention.
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
      <li class='work'>
        More challenging puzzles.
      </li>
      <li class='work'>
        More information about superposition.
      </li>
      <li class='work'>
        Sound effects and background music to enhance immersion.
      </li>
      <li class='work'>
        Social features to enhance engagement.
      </li>
      <li class='work'>
        Translation to more languages.
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
    height: 450px;
    width: 450px;
    padding: 1em;
  }

  ul li {
    margin-bottom: 1em;
  }
</style>
