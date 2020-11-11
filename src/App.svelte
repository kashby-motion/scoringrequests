<script>
  let costOfDelay = 1;
  let effort = 1;
  let confidence = 1;
</script>

<style>
  main {
    text-align: left;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      --blue: #007bff;
      --grey-shadow: rgba(0, 0, 0, 0.15);
      --grey: #cbd5e0;
      padding: 4em;
      max-width: 600px;
    }
    h2 {
      font-family: Roboto;
      font-style: normal;
      font-weight: normal;
      font-size: 24px;
      line-height: 28px;
      margin: 72px 0 0 0;
      color: #000000;
    }
    p {
      font-family: Roboto;
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 16px;
      letter-spacing: 0em;
      text-align: left;
      color: #828181;
      margin: 8px 0 16px;
    }
    h1 {
      font-family: Roboto;
      font-style: normal;
      font-weight: normal;
      font-size: 40px;
      line-height: 47px;

      color: #000000;
    }
    /* input[type="range"] {
      height: 34px;
      -webkit-appearance: none;
      margin: 10px 0;
      width: 100%;
    }
    input[type="range"]:focus {
      outline: none;
    }
    input[type="range"]::-webkit-slider-runnable-track {
      width: 100%;
      height: 15px;
      cursor: pointer;
      animate: 0.2s;
      background: var(--blue);
      border-radius: 8px;
    }
    input[type="range"]::-webkit-slider-thumb {
      box-shadow: 1px 1px 10px var(--grey-shadow);
      border: 1px solid var(--grey);
      height: 40px;
      width: 40px;
      border-radius: 40px;
      background: #ffffff;
      cursor: pointer;
      -webkit-appearance: none;
      margin-top: -15px;
    }
    input[type="range"]:focus::-webkit-slider-runnable-track {
      background: var(--blue);
    }
    input[type="range"]::-moz-range-track {
      width: 100%;
      height: 11px;
      cursor: pointer;
      animate: 0.2s;
      background: var(--blue);
      border-radius: 1px;
    }
    input[type="range"]::-moz-range-thumb {
      box-shadow: 1px 1px 10px var(--grey-shadow);
      border: 1px solid var(--grey);
      height: 26px;
      width: 26px;
      border-radius: 15px;
      background: #ffffff;
      cursor: pointer;
    }
    input[type="range"]::-ms-track {
      width: 100%;
      height: 11px;
      cursor: pointer;
      animate: 0.2s;
      background: transparent;
      border-color: transparent;
      color: transparent;
    }
    input[type="range"]::-ms-fill-lower {
      background: var(--blue);
      border-radius: 2px;
    }
    input[type="range"]::-ms-fill-upper {
      background: var(--blue);
      border-radius: 2px;
    }
    input[type="range"]::-ms-thumb {
      margin-top: 1px;
      box-shadow: 1px 1px 10px var(--grey-shadow);
      border: 1px solid var(--grey);
      height: 26px;
      width: 26px;
      border-radius: 15px;
      background: #ffffff;
      cursor: pointer;
    }
    input[type="range"]:focus::-ms-fill-lower {
      background: var(--blue);
    }
    input[type="range"]:focus::-ms-fill-upper {
      background: var(--blue);
	} */
    input[type="number"] {
      height: 48px;
      width: 72px;
      padding: 8px;
    }
  }
</style>

<main>
  <section>
    <h2>What is the Cost of Delay?</h2>
    <p>Value this provides for our customer</p>
    <label>
      <input type="number" bind:value={costOfDelay} min="1" max="5" />
      <!-- <input type="range" bind:value={costOfDelay} min="1" max="5" /> -->
    </label>
  </section>
  <section>
    <h2>What is the Effort?</h2>
    <p>How hard will it be to build, product and dev</p>
    <label>
      <input type="number" bind:value={effort} min="1" max="5" />
      <!-- <input type="range" bind:value={effort} min="1" max="5" /> -->
    </label>
  </section>
  <section>
    <h2>What is your confidence?</h2>
    <p>How hard will it be to build, product and dev</p>
    <label>
      <input type="number" bind:value={confidence} min="1" max="100" />
      %
      <!-- <input type="range" bind:value={confidence} min="1" max="100" /> -->
    </label>
  </section>
  <section>
    <h2>Final Score</h2>
    <p>({costOfDelay} / {effort}) * {confidence}%</p>
    <h1>{(costOfDelay / effort) * (confidence / 100)}</h1>
  </section>
</main>
