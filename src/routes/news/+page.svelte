<script>
    import Newo from '../../lib/components/Newo.svelte';
</script>
<style>
.container {
    display: grid;
    grid-gap: 5px;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    grid-template-rows: repeat(0, minmax(300px, 0.33fr));
}
</style>

<div class="container">
<Newo title="News" slogan="Very interesting news" link="https://google.com">
    Newnewnewnewnewnewnewnewnewnewnewsss..........
</Newo>
</div>
<Newo title="Second new" slogan="This is news!">What`s happen?</Newo>

</div>