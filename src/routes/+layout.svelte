<script lang="ts">
    import "../app.css";
    import "@picocss/pico/css/pico.classless.css";
</script>

<header>
    <nav class="text-xl">
        <div class="p-5 absolute flex justify-between w-full">
            <strong>mtfirmansyah</strong>
            <div class="md:contents hidden">
                <div class="flex gap-20 text-blue-500">
                    <span><a href="/#education">Educations</a></span>
                    <span><a href="/#experience">Experiences</a></span>
                    <span><a href="/#skill">Skills</a></span>
                </div>
            </div>
        </div>

        <details class="absolute p-5 w-full md:hidden">
            <summary class="flex justify-end">Menu</summary>
            <div class="py-5 text-blue-500">
                <div role="button"><a href="/#education">Educations</a></div>
                <div role="button"><a href="/#experience">Experiences</a></div>
                <div role="button"><a href="/#skill">Skills</a></div>
            </div>
        </details>
    </nav>
</header>
<slot />
<footer class="pb-5 flex justify-center">&copy; 2024, Muchammad Tegar Firmansyah</footer>
