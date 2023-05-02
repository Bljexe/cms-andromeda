<template>
<footer>
    <a>© Copyright, Andromeda Software</a>
    <a href="https://github.com/Bljexe"><img src="../assets/github.png" alt="Github Icon" id="github-social"></a>
</footer>
</template>

<script>
    export default{
        name: 'Footer'
    }
</script>

<style scoped>

footer{
    color: var(--color-text-light);
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.5rem;
}

#github-social{
    width: 25px;
}

</style>