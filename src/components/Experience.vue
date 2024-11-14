<template>
    <section class="container">
        <h2>Experience</h2>
        <section class="jobs">
            <article>
                <div class="dot"></div>
                <div class="place">
                    <h3>Mine KPIs</h3>
                    <h4>from 2022 to 2024</h4>
                </div>
                <div class="job_description">
                    <h3>Software Architecture & Front-end</h3>
                    <p>I developed and maintained the front-end of the web application "BlockNode Operations App" that was useful in the IoT field, especially in the supply chain where the process efficiency was accelerated and enhanced.</p>
                    <p>My development was focused on various web programming languages such as JavaScript, HTML and CSS, in addition to the use of teamwork tools such as Jira, Figma, Skype and Discord, continuously contributing to the improvement of the process in the supply chain.</p>
                    <p>I used several APIs that facilitate the communication of the physical system with the information necessary to obtain the KPIs through data science, the most notable were Web NFC API, Sensor APIs, and Battery Status API, which defined a great advance in the management of product storage and distribution using the web application.</p>
                </div>
            </article>
            <article>
                <div class="dot"></div>
                <div class="place">
                    <h3>Freelance</h3>
                    <h4>from 2020 to 2022</h4>
                </div>
                <div class="job_description">
                    <h3>Engineer in Computed Systems</h3>
                    <p>I developed and designed the web application "Movies Storage" that was very useful to a little community that need a guide to find the location of some movies in their storage.</p>
                    <p>I learned and improve my programming logic doing little practices to later create projects with greater meaning for people with needs, development of ideas and solving problems.</p>
                    <p>I started with web technologies such as HTML, JavaScript, and CSS, and then continued to grow with frameworks such as NodeJS and VueJS that speed up the development of websites and web applications considerably.</p>
                    <p>Currently I have not stopped learning the technologies that I already know for the optimization of the projects I work on, as well as new technologies specialized in the web Front-end such as React or Angular.</p>
                </div>
            </article>
        </section>
    </section>
</template>

<script setup></script>

<style scoped>
section.container {
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

    &>section.jobs {
        display: flex;
        flex-direction: column;
        margin-top: 2.5rem;
        gap: 2rem;

        &>article {
            position: relative;
            display: flex;
            flex-direction: row;
            align-items: start;
            width: 100%;
            min-height: 100px;
            height: fit-content;


            &>div {
                &.dot {
                    display: block;
                    width: 2.5rem;
                    height: 2.5rem;
                    flex-shrink: 0;
                    background-color: var(--accent-color);
                    border-radius: 50%;

                    &::before {
                        content: '';
                        display: flex;
                        position: absolute;
                        margin-left: 1.188rem;
                        background: linear-gradient(to bottom, var(--accent-color) 66%, transparent);
                        width: 0.125rem;
                        height: 100%;
                    }
                }

                &.place {
                    display: flex;
                    flex-direction: column;
                    width: 100%;
                    min-width: 234px;
                    max-width: 324px;
                    flex-shrink: 0;
                    padding: 0 1.5rem 0 1rem;

                    &>h3 {
                        font-size: 2.5rem;
                        line-height: 1;
                        color: var(--color-heading);
                    }

                    &>h4 {
                        font-size: 1rem;
                        line-height: 2;
                    }
                }

                &.job_description {
                    display: flex;
                    flex-direction: column;
                    padding: 0 0.5rem;
                    flex-grow: 1;
                    gap: 0.75rem;

                    &>h3 {
                        font-size: 1.5rem;
                        line-height: normal;
                        color: var(--color-heading);
                    }

                    &>p {
                        font-size: 1.125rem;
                        line-height: normal;
                    }
                }
            }
        }
    }
}
</style>