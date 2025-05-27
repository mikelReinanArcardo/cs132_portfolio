<script>
    let {number=0, question, alt, nul} = $props();
</script>

<section class="flex flex-col justify-center text-white gap-8 text-xl">
    <div class="flex flex-col gap-2 p-12 bg-hpq rounded-xl shadow-sm shadow-lightblue">
            <p class="text-lightblue font-medium">
                Q{number}:
            </p>
            <p class="text-2xl">
                {question}
            </p>
    </div>
    <div class="flex gap-12">
        <div class="flex flex-col gap-4 p-8 bg-hpa rounded-xl shadow-md shawdow-hpq w-full">
            <p class="text-lightblue font-medium">
                Alternative Hypothesis:
            </p>
            <p>
                {alt}
            </p>
        </div>
        <div class="flex flex-col gap-4 p-8 bg-hpa rounded-xl shadow-md shawdow-hpq w-full">
            <p class="text-lightblue font-medium">
                Null Hypothesis:
            </p>
            <p>
                {nul}
            </p>
        </div>
    </div>
</section>