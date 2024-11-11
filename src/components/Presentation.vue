<template>
    <section>
        <article>
            <figure class="profile">
                <img src="../assets/test_image.jpeg" alt="Profile Picture" loading="lazy" title="Leonardo Alvarez" />
            </figure>
            <header>
                <hgroup class="presentation">
                    <h2>Hi, I'm</h2>
                    <h1>Leonardo Alvarez</h1>
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
                    <a href="#contact" class="contact_me">Contact Me!</a>
                    <a href="" class="resume">Get Resume</a>
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
    padding-top: 40px;
    margin-bottom: 40px;

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
            display: flex;
            position: relative;
            width: 100%;
            min-width: 234px;
            max-width: 324px;
            border-radius: 2rem;
            overflow: hidden;

            
            & img {
                object-fit: cover;
                width: 100%;
                transition: all ease 0.2s;

                &:hover {
                    transform: scale(1.25);
                }
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
                max-width: 600px;
                text-align: end;
                margin: 2rem 0 0 0;

                & h2 {
                    font-size: 1.5rem;
                    transition: all ease 0.2s;
                }

                & h1 {
                    font-size: 4.5rem;
                    color: var(--accent-color);
                    line-height: 1;
                    transition: all ease 0.2s;
                }

                & p {
                    font-size: 2rem;
                    line-height: 2;
                }
            }

            & > section.presentation.information {
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                align-items: end;
                height: fit-content;

                & > article {
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    text-align: center;
                    width: 100%;
                    min-width: 228px;
                    max-width: 228px;
                    height: 100%;
                    min-height: 100px;
                    max-height: 182px;
                    gap: 0;
                    border-radius: 2rem;
                    border: 2px solid transparent;
                    transition: all ease 0.2s;
                    padding: 0.5rem;

                    & h1 {
                        height: 100%;
                        align-content: end;
                        font-size: 4rem;
                        color: var(--accent-color);
                    }

                    & p{
                        font-size: 1.2rem;
                    }
                }

                & > article:last-child {
                    & h1 {
                        height: 100%;
                        align-content: center;
                        font-size: 3rem;
                    }

                    & p {
                        font-size: 1rem;
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

                & >a {
                    display: flex;
                    position: relative;
                    height: 60px;
                    width: 150px;
                    border-radius: 50px;
                    align-items: center;
                    cursor: pointer;
                    text-transform: uppercase;
                    justify-content: center;
                    font-size: 1rem;
                    font-weight: bold;
                    transition: all ease 0.2s;

                    &.contact_me {
                        background-color: var(--accent-color);
                        color: var(--color-background);

                        &:hover {
                            text-shadow: 0 0 20px var(--color-background);
                        }
                    }

                    &.resume {
                        background-color: var(--color-background);
                        border: 2px solid var(--accent-color);

                        &:hover {
                            background-color: var(--accent-color);
                            color: var(--color-background);
                            text-shadow: 0 0 20px var(--color-background);
                        }
                    }
                }
            }
        }
    }
}
</style>