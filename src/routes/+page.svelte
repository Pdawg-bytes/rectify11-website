<script lang="ts">
    import { TextBlock } from "fluent-svelte";
    import Card from "../lib/card/card.svelte";

    const featureCards = [
    {
      name: 'Better scaling',
      description: 'Rectify11 makes UI controls consistent on different resolutions and scaling options.',
      hero: "/images/scaling.png"
    },
    {
      name: 'Better UI',
      description: 'We have replaced most legacy icons with modern icons and updated older MetroUI based dialogs.',
      hero: "/images/menusD.png"
    },
    {
      name: 'Truly consistent',
      description: 'We have tried our best to replicate fluent controls in our themes, and add proper darkmode support to most apps.',
      hero: "/images/ui.png"
    },
    {
      name: 'Better performance',
      description: 'In future releases, you will be able to choose things that you want to debloat in your system.',
      hero: "/images/performance.png"
    },
    {
      name: 'Better experience',
      description: 'Rectify11 adds many quality of life improvements to Windows 11, allowing you to be more productive.',
      hero: "/images/cool.png"
    },
  ];
</script>
<div id="container">
	<div id="intro">
        <TextBlock variant="display" style="margin-left: 20px; margin-right: 20px; font-size: 60px;">Introducing Rectify11</TextBlock>
        <TextBlock variant="bodyLarge" style="margin-top: 8px; margin-left: 20px; margin-right: 20px;">Improving upon the Windows 11 experience.</TextBlock>
    </div>
    <div id="card-container">
        {#each featureCards as featureCard}
            <Card bind:name={featureCard.name} bind:description={featureCard.description} bind:hero={featureCard.hero}/>
        {/each}
    </div>
</div>

<style>
	#container
    {
        background-color: var(--fds-solid-background-base);
        background-size: cover; 
        width: 100vw;
		    min-height: 100vh;
        text-align: center;
        background: url("/src/lib/dark_bg.png") no-repeat center center fixed;
        background-size: cover;
        display: flex;
        flex-direction: column;
        overflow: auto;
        overflow-x: hidden;
        overflow-y: hidden;
    }
    @media (prefers-color-scheme: light) {
        #container 
        {
            background-image: url("/src/lib/light_bg.png");
        }
    }

    #intro
    {
        display: flex;
        flex-direction: column;
        width: auto;
        height: auto;
        margin-top: 100px;
    }

    #card-container
    {
        width: 100vw;
        min-height: 225px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin-top: 70px;
        vertical-align: middle;
    }
</style>

<head>
  <title>Rectify11 • Home</title>
</head>