<script>
    import "iconify-icon";
    import photo from "$lib/images/photo.jpg";
    import socialData from "$lib/data/social.json";
    import educationData from "$lib/data/education.json";
    import experienceData from "$lib/data/experience.json";
    import certificationData from "$lib/data/certification.json";
    import skillData from "$lib/data/skill.json";
    import EducationCard from "$lib/EducationCard.svelte";
    import ExperienceCard from "$lib/ExperienceCard.svelte";
    import CertificationList from "$lib/CertificationList.svelte";
</script>

<svelte:head>
    <title>mtirmansyah | Portfolio</title>
</svelte:head>
<main class="p-10 container mx-auto">
    <section class="md:flex md:gap-10 pt-[5rem]">
        <img class="h-[20rem] my-5 mx-auto rounded-lg" src={photo} alt="" />
        <div class="">
            <h1 class="py-5">Muchammad Tegar Firmansyah</h1>
            <a class="py-5 text-xl text-blue-500" href="mailto:mtfirmansyah15@gmail.com">mtfirmansyah15@gmail.com</a>
            <p class="py-5 text-xl">
                Electrical Engineering student at Sepuluh Nopember Intitute of Technology. Specializing in Multimedia Telecommunication with a primary focus on RF Engineering and Web Development. Practical experience includes working on
                various front-end projects utilizing technologies such as Javascript, Node.js, and React with Next JS web framework.
            </p>
            <figure class="py-5 flex gap-5 text-5xl">
                {#each socialData as social}
                    <a href={social.link}><iconify-icon icon={social.icon} data-tooltip={social.tooltip} /></a>
                {/each}
            </figure>
        </div>
    </section>
    <section class="py-5" id="education">
        <h2 class="pb-5">Educations</h2>
        <div>
            {#each educationData as education}
                <EducationCard school={education.school} url={education.url} major={education.major} start={education.start} end={education.end} description={education.description} />
            {/each}
        </div>
    </section>
    <section class="py-5" id="experience">
        <h2 class="pb-5">Experiences</h2>
        <div>
            {#each experienceData as experience}
                <ExperienceCard job={experience.job} company={experience.company} url={experience.url} start={experience.start} end={experience.end} description={experience.description} />
            {/each}
        </div>
    </section>
    <section class="py-5" id="skill">
        <h2 class="pb-5">Skills</h2>
        <div>
            <article>
                <h3>Electronics and RF</h3>
                <figure class="text-5xl text-center">
                    {#each skillData.electronicsAndRF as skill}
                        <iconify-icon class="px-2" icon={skill.icon} data-tooltip={skill.tooltip}></iconify-icon>
                    {/each}
                </figure>
            </article>
            <article>
                <h3>Network Technology</h3>
                <figure class="text-5xl text-center">
                    {#each skillData.networkTechnology as skill}
                        <iconify-icon class="px-2" icon={skill.icon} data-tooltip={skill.tooltip}></iconify-icon>
                    {/each}
                </figure>
            </article>
            <article>
                <h3>Web Development</h3>
                <div class="text-5xl text-center">
                    {#each skillData.webDevelopment as skill}
                        <iconify-icon class="px-2" icon={skill.icon} data-tooltip={skill.tooltip}></iconify-icon>
                    {/each}
                </div>
            </article>
        </div>
    </section>
    <section class="py-5" id="certification">
        <h2 class="pb-5">Certifications</h2>
        <ul class="text-xl">
            {#each certificationData as certification}
                <CertificationList title={certification.title} />
            {/each}
        </ul>
    </section>
</main>
