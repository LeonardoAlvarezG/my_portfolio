<template>
    <section>
        <article>
            <figure class="profile">
                <img src="../assets/test_image.jpeg" alt="Profile Picture" loading="lazy" title="Leonardo Alvarez" />
            </figure>
            <header>
                <hgroup class="presentation">
                    <h1>Hi, I'm Leonardo Alvarez</h1>
                    <p>Front-End Web Developer</p>
                </hgroup>
                <section class="presentation information">
                    <article>
                        <h1>+3</h1>
                        <p>years of experience</p>
                    </article>
                    <article>
                        <h1>3</h1>
                        <p>solutions developed</p>
                    </article>
                    <article>
                        <h1>Engineer</h1>
                        <p>in Computed Systems</p>
                    </article>
                </section>
                <section class="presentation contact">
                    <button class="contact_me">Contact Me!</button>
                    <button class="resume">Get Resume</button>
                </section>
            </header>
        </article>
    </section>
</template>

<script setup></script>

<style scoped>
section {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: fit-content;
    justify-content: center;

    & > article {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        position: relative;
        z-index: 1;
        width: 100%;
        min-width: 500px;
        max-width: 1056px;
        height: fit-content;
        gap: 1rem;
        
        & > figure.profile {
            position: relative;
            width: 100%;
            min-width: 234px;
            max-width: 324px;
            
            & img {
                object-position: contain;
                width: 100%;
                border-radius: 2rem;
            }
        }

        & > header {
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            align-items: end;
            width: 100%;
            padding: 0 1rem;

            & > hgroup.presentation {
                width: 100%;
                min-width: 234px;
                max-width: 324px;
                text-align: end;
            }

            & > section.presentation.information {
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                align-items: center;
                height: fit-content;

                & > article {
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    text-align: center;
                    width: 100%;
                    min-width: 150px;
                    max-width: 200px;
                    height: 100%;
                    min-height: 132px;
                    max-height: 182px;
                    gap: 0;

                    & h1 {
                        height: 100%;
                        align-content: end;
                        font-size: 4rem;
                    }
                }

                & > article:last-child {
                    & h1 {
                        height: 100%;
                        align-content: end;
                        font-size: 3rem;
                    }
                }
            }

            & > section.presentation.contact {
                display: flex;
                flex-direction: row;
                justify-content: space-around;
                width: 100%;
                min-width: 200px;
                max-width: 400px;
                height: fit-content;
                align-self: center;

                & button {
                    position: relative;
                    height: 60px;
                    width: 150px;
                    border-radius: 50px;
                    text-transform: uppercase;
                    justify-content: center;
                    align-items: center;
                    cursor: pointer;
                    transition: all ease 0.2s;

                    &.contact_me {
                        background-color: var(--accent-color);

                        &:hover {
                            color: var(--color-heading);
                        }
                    }

                    &.resume {
                        background-color: var(--color-background);
                        border: 2px solid var(--accent-color);

                        &:hover {
                            background-color: var(--accent-color);
                            color: var(--color-heading);
                        }
                    }
                }
            }
        }
    }
}
</style>