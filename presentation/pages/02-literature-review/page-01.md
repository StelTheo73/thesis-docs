# Design & Development Process

<p class='slide-subtitle'>Overview (2/3)</p>

<div class='section-wrapper'>
  <div class='img-caption-wrapper'>
    <div class='image-wrapper grey-shadow bg-white-smoke rounded-md'>
      <img src='../../assets/images/design/design_flow.png'/>
    </div>
    <span>Figure 1: Educational Game Design.<Link class='ref-link' to=''>[1]</Link></span>
  </div>
  <div class='text-wrapper'>
    <div class='card grey-shadow rounded-md fade-out-vclick' v-after='+1'>
      <h4><strong>1. Technology: Flutter Framework & Flame Game Engine</strong></h4>
      <ul class=''>
        <li>Single codebase</li>
        <li>Lower development cost</li>
        <li>Lower maintenance cost</li>
        <li>Balance between performance and cost</li>
        <li>Libraries for quantum circuits simulation</li>
      </ul>
    </div>
    <div class='card grey-shadow rounded-md fade-out-vclick' v-click='+1'>
      <h4><strong>2. Pedagogy</strong></h4>
      <ul class=''>
        <li>Research for quantum mechanics concepts</li>
        <li>Research for similar educational games to define educational content</li>
      </ul>
    </div>
  </div>
</div>

<style>
  .section-wrapper {
    margin-top: -2em;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
  }

  .text-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
  }

  .text-wrapper .card {
    margin: 1em;
    padding: 1em;
  }

  .image-wrapper img {
    height: 500px;
    padding: 0.5em;
  }
</style>
