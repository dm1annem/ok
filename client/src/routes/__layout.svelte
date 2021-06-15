<script>
import "../app.postcss";
import MyHeader from '$lib/components/site/layouts/header/Header.svelte';
import MyFooter from '$lib/components/site/layouts/footer/Footer.svelte';
</script>

<MyHeader/>

<slot></slot>

<MyFooter/>