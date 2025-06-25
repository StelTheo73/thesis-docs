# Design and Development Process

<p class='slide-subtitle'>Conceptual Design (1/2)</p>

<div class='section-wrapper'>
  <div class='image-wrapper grey-shadow bg-white-smoke rounded-md'>
    <img src='../../assets/conceptual-design.png'/>
  </div>
  <div class='text-wrapper'>
    <div class='section-1'>
      <p>
        According to Kalmpourtzis (2018)<Link class='ref-link' to=''>[1]</Link>, there are five elements to consider when designing an educational game: Pedagogy, Mechanics, Technology, Aesthetics, and Narratives.
      </p>
      <p>
        Having already chosen the technologies we will use, we proceeded with the design process around 3 dimensions: Pedagogy, Mechanics, and Aesthetics-Narratives.
      </p>
    </div>
    <hr class='divider-2' v-click='+1'/>
    <div class='section-2'
      v-click='+1'
      v-motion
      :initial="{ y: -80 }"
      :enter="{ y: 0 }"
    >
      <ol class='ol-flex'>
        <li><p><strong>Pedagogy:</strong> Quantum Computing concepts to include in the game</p>
          <ul>
            <li>Quantum Bits</li>
            <li>Quantum Registers</li>
            <li>Quantum Gates: Pauli-X, Pauli-Y, Pauli-Z, Hadamard</li>
            <li>Superposition</li>
          </ul>
        </li>
      </ol>
    </div>
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

  .section-2 {
    display: flex;
  }

  ol > li > p {
    font-size: larger;
    text-decoration: underline;
  }

  .image-wrapper {
    padding: 0.5em;
    height: max-content;
  }

  .image-wrapper img {
    width: 550px;
    height: 450px;
  }
</style>
