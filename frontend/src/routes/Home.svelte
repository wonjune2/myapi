<script>
    import { link } from 'svelte-spa-router';
    import fastapi from "../lib/api";

    let question_list = []

    fastapi('get', '/api/question/list', {}, (json) => {
        question_list = json
    })
</script>

<ul>
    {#each question_list as question}
        <li><a use:link href="/detail/{question.id}">{question.subject}</a></li>
    {/each}
</ul>
