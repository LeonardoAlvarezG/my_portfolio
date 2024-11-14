<template>
    <footer>
        <section class="title">
            <h3>Leonardo Manuel Alvarez Gonzalez</h3>
        </section>
        <div class="divider"></div>
        <section class="information">
            <h4 class="title">My Portfolio</h4>
            <ul class="technologies">
                <li><LanguageTag  :lang_tag="'VUE'" /></li>
            </ul>
            <button class="source_code" data-tooltip="Source Code">
                <GitHubLogo class="logo" />
                Source Code
            </button>
        </section>
    </footer>
</template>

<script setup>
import LanguageTag from './LanguageTag.vue';
import GitHubLogo from './icons/GitHubLogo.vue';
</script>

<style scoped>
    footer {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 200px;
        background-color: var(--color-background-mute);
        padding: 1.5rem 2rem;

        &>section {
            display: flex;
            flex-direction: column;
            width: 300px;

            &.title {
                color: var(--color-heading);
            }

            &.information {
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 1rem;

                &>h4.title {
                    height: fit-content;
                    color: var(--color-heading);
                }

                &>ul.technologies {
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    justify-content: center;
                    flex-wrap: wrap;
                    list-style-type: none;
                    padding: 0;
                }

                &>button {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: fit-content;
                    height: fit-content;
                    min-height: 40px;
                    position: relative;
                    font-weight: 600;
                    border: solid 1px var(--color-heading);
                    border-radius: 40px;
                    padding: 0.5rem 1rem;
                    cursor: pointer;
                    transition: background 0.3s ease,
                                color 0.3s ease,
                                border 0.3s ease;

                    &.source_code {
                        font-size: 14px;

                        &>svg.logo {
                            width: 24px;
                            height: 24px;
                            aspect-ratio: 1/1;
                            margin: 0 0.5rem 0 0;
                        }
                    }

                    &:not(:disabled):hover {
                        background-color: var(--accent-color);
                        color: var(--color-background);
                        border: solid 1px var(--accent-color);

                        &>svg.logo.GitHub {
                            &:deep(path) {
                                fill: var(--color-background);
                            }
                        }
                    }
                }
            }
        }

        &>div.divider {
            content: '';
            display: flex;
            width: 2px;
            height: 80%;
            background: linear-gradient(to bottom, var(--color-heading) 66%, transparent);
            margin: 0 2rem;
        }
    }
</style>