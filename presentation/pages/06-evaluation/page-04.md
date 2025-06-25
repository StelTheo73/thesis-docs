# Evaluation

<p class='slide-subtitle'>Pre-Post Tests 2/2: Results</p>

<div class='section-wrapper'>
  <div class='grey-shadow rounded-md'>
    <ul class='flex-list none'>
      <li class='check mb2 fade-out-vclick' v-after>
        <span>
          Pre Test Average Score: <strong>17%</strong>.<br>
          Post Test Average Score: <strong>75%</strong>.
        </span>
        <span class='fast-forward'></span>
        <span>
          Significant improvement in scores after playing the game.
        </span>
      </li>
      <li class='check mb2 fade-out-vclick' v-click='+1'>
        <span>Paired t-test: <strong>p-value < 0.001</strong></span>
        <span class='fast-forward'></span>
        <span>
          Difference between average scores is significant.
        </span>
      </li>
      <li class='check mb2 fade-out-vclick' v-click='+2'>
        <span>Average Normalized Gain: <strong>0.7</strong>.</span>
        <span class='fast-forward'></span>
        <span>
          Well above the 0.25 effectiveness threshold.
          <Link class='ref-link' to=''>[3]</Link><Link class='ref-link' to=''>[4]</Link>
        </span>
      </li>
      <li class='check mb2 fade-out-vclick' v-click='+3'>
        <span>Retention Test Average Score: <strong>55%</strong>.</span>
        <span class='fast-forward'></span>
        <span>Players retained knowledge effectively.</span>
      </li>
      <li class='warn fade-out-vclick' v-click='+4'>
        <span>Positive correlation between <strong>higher scores</strong> and <strong>academic background</strong>.</span>
        <span class='fast-forward'></span>
        <span>Strong background in Physics and Computer Science.</span>
      </li>
    </ul>
  </div>
</div>

<style>
  .section-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 65%;
  }

  .section-wrapper div {
    max-width: max-content;
    padding: 2em;
  }

  li.mb2 {
    margin-bottom: 0.7em;
  }

  li {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    width: 800px;
  }

  li > span:nth-child(1) {
    min-width: 300px;
    max-width: 300px;
  }

  li > span:nth-child(2) {
    min-width: 50px;
    max-width: 50px;
    text-align: center;
  }

  li > span:nth-child(3) {
    min-width: 300px;
    max-width: 300px;
  }
</style>
