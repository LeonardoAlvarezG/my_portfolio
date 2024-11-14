<template>
    <section>
        <article>
            <h3>Let's start together!</h3>
            <p>I am sure that together we can create the project you have in mind!</p>
            <button>Contact Me</button>
        </article>
    </section>
</template>

<script setup>

</script>

<style scoped>
section {
    display: flex;
    margin: 40px 0;
    background-color: var(--color-background-soft);
    padding: 2rem;
    border-radius: 0.5rem;

    &>article {
        display: flex;
        flex-direction: column;
        width: fit-content;
        max-width: 1056px;
        gap: 1rem;

        &>h3 {
            font-size: 3rem;
            color: var(--color-heading);
            line-height: 1;
        }

        &>p {
            font-size: 1.5rem;
        }

        &>button {
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            width: fit-content;
            height: fit-content;
            min-height: 52px;
            border: solid 1px var(--accent-color);
            border-radius: 52px;
            background-color: var(--accent-color);
            color: var(--color-background);
            padding: 0.875rem 1.5rem;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: border ease 0.3s,
                        text-shadow ease 0.3s;

            &:hover {
                border: solid 1px var(--color-heading);
                text-shadow: 0 0 20px var(--color-background);
            }
        }
    }
}
</style>