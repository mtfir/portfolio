<script>
    let { school, url, major, start, end, description } = $props();
</script>

<article>
    <h3 class="text-blue-500"><a href={url}>{school}</a></h3>
    <h4>{major}</h4>
    <h5>{start} - {end}</h5>
    <p>{description}</p>
</article>
