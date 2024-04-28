<script>
    let { job, company, url, start, end, description } = $props();
</script>

<article>
    <h3>{job}</h3>
    <h4 class="text-blue-500"><a href={url}>{company}</a></h4>
    <h5>{start} - {end}</h5>
    <details>
        <summary>Job Description </summary>
        <p>{description}</p>
    </details>
</article>
