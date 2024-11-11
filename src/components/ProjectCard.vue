<template>
    <article class="card">
        <section class="header">
            <img class="image" src="../assets/mexico-flag.png" alt="">
        </section>
        <section class="body">
            <h3 class="title">{{project_title}}</h3>
            <p class="short_description">{{short_description}}</p>
            <ul class="technologies">
                <li v-for="language in technologies"><LanguageTag  :lang_tag="language" /></li>
            </ul>
        </section>
        <section class="footer">
            <button class="source_code" data-tooltip="Source Code">
                <GitLabLogo v-if="platform === 'GitLab'" class="logo" />
                <GitHubLogo v-else class="logo" />
                Source Code
            </button>
            <button class="details">Details</button>
        </section>
    </article>
</template>

<script setup>
import GitHubLogo from './icons/GitHubLogo.vue';
import GitLabLogo from './icons/GitLabLogo.vue';
import LanguageTag from './LanguageTag.vue';

defineProps({ project_title: String, short_description: String, technologies: Object, platform: String })
</script>

<style scoped>
    article.card {
        display: flex;
        flex-direction: column;
        align-items: start;
        width: 300px;
        min-height: 500px;
        height: fit-content;
        background-color: var(--color-background-soft);
        border-radius: 0.5rem;

        &>section.header {
            display: flex;
            width: 100%;
            
            &>img.image {
                width: 100%;
                aspect-ratio: 16/9;
                object-fit: fill;
                border-radius: 0.5rem 0.5rem 0 0;
                background-color: var(--color-background-soft);
            }
        }

        &>section.body {
            display: flex;
            flex-direction: column;
            flex-grow: 1;
            align-items: start;
            background-color: var(--color-background-soft);

            &>h3.title {
                width: 100%;
                height: fit-content;
                padding: 1rem 1rem 0.5rem;
                color: var(--color-heading);
            }

            &>p.short_description {
                display: flex;
                flex-grow: 1;
                width: 100%;
                height: fit-content;
                min-height: 100px;
                padding: 0 1rem 1rem;
            }

            &>ul.technologies {
                display: flex;
                flex-direction: row;
                align-items: center;
                justify-content: space-between;
                flex-wrap: wrap;
                padding: 0 1rem 1rem;
                list-style-type: none;
                gap: 1rem;
            }
        }

        &>section.footer {
            display: flex;
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            height: fit-content;
            min-height: 48px;
            padding: 0 1rem 1rem;
            gap: 1rem;

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

                &.details {
                    flex-grow: 1;
                    height: 42px;
                    font-size: 14px;
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

            &>div {
                display: flex;
                justify-content: center;
                align-items: center;
                width: fit-content;
                height: fit-content;
                position: relative;

                &::after {
                    content: attr(data-tooltip);
                    visibility: hidden;
                    width: 108px;
                    background-color: var(--color-background);
                    color: var(--color-text);
                    text-align: center;
                    border-radius: 8px;
                    padding: 4px 8px;
                    position: absolute;
                    z-index: 1;
                    top: 110%;
                    left: 50%;
                    transform: translateX(-50%);
                    opacity: 0;
                    transition: opacity 0.3s;
                    border: solid 1px var(--color-heading);
                }

                &>svg.logo {
                    width: 32px;
                    height: 32px;
                    aspect-ratio: 1/1;
                }

                &:hover::after {
                    visibility: visible;
                    opacity: 1;
                }
            }
        }
    }
</style>