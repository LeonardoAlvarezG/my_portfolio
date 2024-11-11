<template>
    <section>
        <h2>Projects</h2>
        <section>
            <ProjectCard 
                :project_title="'BlockNode Operations App'" 
                :short_description="'Web application that supports companies included in the supply chain, greatly speeding up the management of various processes.'" 
                :technologies="['HTML', 'CSS', 'JS']" 
                :platform="'GitLab'" />
            <ProjectCard 
                :project_title="'Movies Storage'" 
                :short_description="'Web application that manages the location of movie storage in scattered storage.'" 
                :technologies="['VUE', 'HTML', 'CSS', 'JS']" 
                :platform="'GitHub'" />
            <ProjectCard 
                :project_title="'Restaurant Manager'" 
                :short_description="'Web Application that bring support to a little restaurant, include service to clients and waiters.'" 
                :technologies="['VUE', 'HTML', 'CSS', 'JS']" 
                :platform="'GitHub'" />
        </section>
    </section>
</template>

<script setup>
    import ProjectCard from './ProjectCard.vue';
</script>

<style scoped>
    section {
        display: flex;
        flex-direction: column;
        width: 100%;
        min-width: 500px;
        max-width: 1056px;
        height: fit-content;
        justify-content: center;
        z-index: 1;

        &>h2 {
            font-size: 4.25rem;
            line-height: 1;
            color: var(--color-heading);
        }

        &>section {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 2.5rem;
        }
    }
</style>