<script>
    let {question, answer} = $props();
</script>

<section class="flex flex-col justify-center text-white gap-8 text-lg md:text-xl">
    <div class="flex flex-col gap-2 p-8 md:p-12 bg-hpq rounded-xl shadow-sm shadow-lightblue">
        <p class="text-lightblue text-xl md:text-2xl">
            {question}
        </p>
        <p>
            {answer}
        </p>
    </div>
</section>