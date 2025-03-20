<script>
  import projects from "$lib/projects.json";
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<br/>
    
    <h1>{ projects.length } Projects</h1>
    <!-- .projects>article*6>h2>lorem4^img[src="https://i.etsystatic.com/iap/a0f246/5502938083/iap_640x640.5502938083_69958kp0.jpg"]+p>lorem -->
    <div class="projects">
          {#each projects as p}
            <article>
                <h2>{p.title}</h2>
                <img src={p.image} alt="" />
                <p>
                    {p.description}
                </p>
            </article>
            {/each}
    </div>