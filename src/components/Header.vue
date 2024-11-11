<template>
    <header>
        <a href="/"><h1>Leonardo Alvarez</h1></a>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#experience">Experience</a></li>
            </ul>
        </nav>
        <div>
            <ul>
                <li>
                    <a href="https://www.linkedin.com/in/leonardo-alvarez-dev98/" target="_blank" title="LinkedIn"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 50 50" class="logo LinkedIn"><path style="fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;" d="M9,45h32c2.209,0,4-1.791,4-4V9c0-2.209-1.791-4-4-4H9C6.791,5,5,6.791,5,9v32C5,43.209,6.791,45,9,45z"/><polygon style="fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;" points="11,20 17,20 17,33.135 17,39 11,39 "/><path style="fill:none;stroke-width:1.9758;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;" d="M14,17L14,17c-1.8,0-3-1.133-3-2.533S12.2,12,14,12s2.925,1.067,3,2.467C17,15.867,15.875,17,14,17z"/><path style="fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:10;" d="M39,39h-6c0,0,0-9.257,0-10c0-2-1-4-3.5-4.043C27.022,24.913,26,27,26,29c0,0.909,0,10,0,10h-6V20h6v2.561c0,0,1.93-2.561,5.813-2.561C35.778,20,39,22.726,39,28.261V39z"/></svg></a>
                </li>
                <li>
                    <a href="https://github.com/LeonardoAlvarezG" target="_blank" title="GitHub"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 98 96" class="logo GitHub"><path fill-rule="evenodd" clip-rule="evenodd" d="M48.854 0C21.839 0 0 22 0 49.217c0 21.756 13.993 40.172 33.405 46.69 2.427.49 3.316-1.059 3.316-2.362 0-1.141-.08-5.052-.08-9.127-13.59 2.934-16.42-5.867-16.42-5.867-2.184-5.704-5.42-7.17-5.42-7.17-4.448-3.015.324-3.015.324-3.015 4.934.326 7.523 5.052 7.523 5.052 4.367 7.496 11.404 5.378 14.235 4.074.404-3.178 1.699-5.378 3.074-6.6-10.839-1.141-22.243-5.378-22.243-24.283 0-5.378 1.94-9.778 5.014-13.2-.485-1.222-2.184-6.275.486-13.038 0 0 4.125-1.304 13.426 5.052a46.97 46.97 0 0 1 12.214-1.63c4.125 0 8.33.571 12.213 1.63 9.302-6.356 13.427-5.052 13.427-5.052 2.67 6.763.97 11.816.485 13.038 3.155 3.422 5.015 7.822 5.015 13.2 0 18.905-11.404 23.06-22.324 24.283 1.78 1.548 3.316 4.481 3.316 9.126 0 6.6-.08 11.897-.08 13.526 0 1.304.89 2.853 3.316 2.364 19.412-6.52 33.405-24.935 33.405-46.691C97.707 22 75.788 0 48.854 0z"/></svg></a>
                </li>
                <li>
                    <div class="dropdown">
                        <button id="settingsButton" title="Settings" @click="ToggleSettings"><svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 50 50" class="logo settings"><path d="M 22.205078 2 A 1.0001 1.0001 0 0 0 21.21875 2.8378906 L 20.246094 8.7929688 C 19.076509 9.1331971 17.961243 9.5922728 16.910156 10.164062 L 11.996094 6.6542969 A 1.0001 1.0001 0 0 0 10.708984 6.7597656 L 6.8183594 10.646484 A 1.0001 1.0001 0 0 0 6.7070312 11.927734 L 10.164062 16.873047 C 9.583454 17.930271 9.1142098 19.051824 8.765625 20.232422 L 2.8359375 21.21875 A 1.0001 1.0001 0 0 0 2.0019531 22.205078 L 2.0019531 27.705078 A 1.0001 1.0001 0 0 0 2.8261719 28.691406 L 8.7597656 29.742188 C 9.1064607 30.920739 9.5727226 32.043065 10.154297 33.101562 L 6.6542969 37.998047 A 1.0001 1.0001 0 0 0 6.7597656 39.285156 L 10.648438 43.175781 A 1.0001 1.0001 0 0 0 11.927734 43.289062 L 16.882812 39.820312 C 17.936999 40.39548 19.054994 40.857928 20.228516 41.201172 L 21.21875 47.164062 A 1.0001 1.0001 0 0 0 22.205078 48 L 27.705078 48 A 1.0001 1.0001 0 0 0 28.691406 47.173828 L 29.751953 41.1875 C 30.920633 40.838997 32.033372 40.369697 33.082031 39.791016 L 38.070312 43.291016 A 1.0001 1.0001 0 0 0 39.351562 43.179688 L 43.240234 39.287109 A 1.0001 1.0001 0 0 0 43.34375 37.996094 L 39.787109 33.058594 C 40.355783 32.014958 40.813915 30.908875 41.154297 29.748047 L 47.171875 28.693359 A 1.0001 1.0001 0 0 0 47.998047 27.707031 L 47.998047 22.207031 A 1.0001 1.0001 0 0 0 47.160156 21.220703 L 41.152344 20.238281 C 40.80968 19.078827 40.350281 17.974723 39.78125 16.931641 L 43.289062 11.933594 A 1.0001 1.0001 0 0 0 43.177734 10.652344 L 39.287109 6.7636719 A 1.0001 1.0001 0 0 0 37.996094 6.6601562 L 33.072266 10.201172 C 32.023186 9.6248101 30.909713 9.1579916 29.738281 8.8125 L 28.691406 2.828125 A 1.0001 1.0001 0 0 0 27.705078 2 L 22.205078 2 z M 23.056641 4 L 26.865234 4 L 27.861328 9.6855469 A 1.0001 1.0001 0 0 0 28.603516 10.484375 C 30.066026 10.848832 31.439607 11.426549 32.693359 12.185547 A 1.0001 1.0001 0 0 0 33.794922 12.142578 L 38.474609 8.7792969 L 41.167969 11.472656 L 37.835938 16.220703 A 1.0001 1.0001 0 0 0 37.796875 17.310547 C 38.548366 18.561471 39.118333 19.926379 39.482422 21.380859 A 1.0001 1.0001 0 0 0 40.291016 22.125 L 45.998047 23.058594 L 45.998047 26.867188 L 40.279297 27.871094 A 1.0001 1.0001 0 0 0 39.482422 28.617188 C 39.122545 30.069817 38.552234 31.434687 37.800781 32.685547 A 1.0001 1.0001 0 0 0 37.845703 33.785156 L 41.224609 38.474609 L 38.53125 41.169922 L 33.791016 37.84375 A 1.0001 1.0001 0 0 0 32.697266 37.808594 C 31.44975 38.567585 30.074755 39.148028 28.617188 39.517578 A 1.0001 1.0001 0 0 0 27.876953 40.3125 L 26.867188 46 L 23.052734 46 L 22.111328 40.337891 A 1.0001 1.0001 0 0 0 21.365234 39.53125 C 19.90185 39.170557 18.522094 38.59371 17.259766 37.835938 A 1.0001 1.0001 0 0 0 16.171875 37.875 L 11.46875 41.169922 L 8.7734375 38.470703 L 12.097656 33.824219 A 1.0001 1.0001 0 0 0 12.138672 32.724609 C 11.372652 31.458855 10.793319 30.079213 10.427734 28.609375 A 1.0001 1.0001 0 0 0 9.6328125 27.867188 L 4.0019531 26.867188 L 4.0019531 23.052734 L 9.6289062 22.117188 A 1.0001 1.0001 0 0 0 10.435547 21.373047 C 10.804273 19.898143 11.383325 18.518729 12.146484 17.255859 A 1.0001 1.0001 0 0 0 12.111328 16.164062 L 8.8261719 11.46875 L 11.523438 8.7734375 L 16.185547 12.105469 A 1.0001 1.0001 0 0 0 17.28125 12.148438 C 18.536908 11.394293 19.919867 10.822081 21.384766 10.462891 A 1.0001 1.0001 0 0 0 22.132812 9.6523438 L 23.056641 4 z M 25 17 C 20.593567 17 17 20.593567 17 25 C 17 29.406433 20.593567 33 25 33 C 29.406433 33 33 29.406433 33 25 C 33 20.593567 29.406433 17 25 17 z M 25 19 C 28.325553 19 31 21.674447 31 25 C 31 28.325553 28.325553 31 25 31 C 21.674447 31 19 28.325553 19 25 C 19 21.674447 21.674447 19 25 19 z"/></svg></button>
                        <div id="settings" class="content">
                            <ul>
                                <li><div class="switchThemeContainer"><input class="switchTheme" type="checkbox" name="ThemeToggle" id="themeToggle" role="switch" v-model="isDark"><div id="switchOption" class="switchOption"></div></div></li>
                                <li class="switchLanguage">
                                    <input type="radio" id="radioSpanish" name="language" value="Spanish" />
                                    <label for="radioSpanish">Spanish</label>
                                </li>
                                <li class="switchLanguage">
                                    <input type="radio" id="radioEnglish" name="language" value="English" />
                                    <label for="radioEnglish">English</label>
                                </li>
                            </ul>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
    </header>
</template>

<script setup>
    import { ref, onMounted } from 'vue';

    const storageTheme = localStorage.getItem('theme');
    const systemColorScheme = window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light';
    const newTheme = storageTheme ?? systemColorScheme;
    let isDark = ref(newTheme === "dark" ? true : false);

    onMounted(()=>{
        const switcherTheme = document.getElementById("themeToggle");
        const root = document.documentElement;
        if (isDark.value) {document.getElementById("switchOption").classList.add("dark");}

        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            const newColorScheme = event.matches ? "dark" : "light";
            isDark.value = newColorScheme === "dark" ? true : false;
            root.setAttribute('data-theme', newColorScheme);
        
            localStorage.setItem('theme', newColorScheme);

            document.getElementById("switchOption").classList.toggle("dark");
        });

        if(root.getAttribute('data-theme') === 'dark'){
            switcherTheme.checked = true;
        }

        switcherTheme.addEventListener("click", ToggleTheme);

        function ToggleTheme() {
            const setTheme = this.checked ? 'dark' : 'light';
            root.setAttribute('data-theme', setTheme);
        
            localStorage.setItem('theme', setTheme);

            document.getElementById("switchOption").classList.toggle("dark");
        }
    });

    function ToggleSettings() {
        document.getElementById("settings").classList.toggle("show");
        document.getElementById("settingsButton").classList.toggle("active");
    };
</script>

<style scoped>
header {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 60px;
    position: sticky;
    top: 0;
    z-index: 100;
    background-color: var(--color-background);

    &>a {
        display: flex;
        transition: color 0.2s ease-in-out;

        &:hover {
            color: var(--accent-color);
        }
    }

    &>nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        height: 100%;
        width: fit-content;

        &>ul {
            display: flex;
            flex-direction: row;
            align-items: center;
            gap: 1rem;
            width: fit-content;
            height: 100%;

            &>li {
                width: fit-content;
                height: 100%;
                display: flex;
                justify-content: center;
                align-items: center;
                
                
                &>a {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    width: fit-content;
                    height: 100%;
                    margin: 0;
                    padding: 0.5rem;
                    border: 1px solid transparent;
                    border-radius: 4px;
                    transition: border 0.2s ease-in-out;

                    &:hover {
                        /* background-image: linear-gradient(to top, var(--accent-color), var(--color-background) 35%); */
                        border: 1px solid var(--accent-color);
                    }
                }
            }
        }
    }

    &>div {
        height: 100%;
        width: fit-content;

        &>ul {
            display: flex;
            flex-direction: row;
            align-items: center;
            width: fit-content;
            height: 100%;
            gap: 1rem;

            & li {
                display: flex;
                align-items: center;
                justify-content: center;
                padding: 0;
                margin: 0;
                width: fit-content;
                height: 100%;

                &>a {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    width: fit-content;
                    height: 100%;

                    & svg.logo>* {
                        transition: all ease 0.3s;
                    }

                    &:hover svg.logo {
                        &.LinkedIn {
                            & path, polygon {
                                stroke: var(--accent-color);
                            }
                        }

                        &.GitHub {
                            & path {
                                fill: var(--accent-color);
                            }
                        }
                    }
                }

                &>div.dropdown {
                    display: inline-block;
                    position: relative;
                    width: fit-content;
                    height: 100%;
                    align-content: center;

                    &>button {
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        width: fit-content;
                        height: 100%;
                        cursor: pointer;

                        &.active svg.logo {
                            transform: rotate(90deg);
                        }

                        &>svg.logo,>svg.logo>* {
                            transition: all ease 0.3s, transform ease-out 0.5s;
                        }

                        &:hover svg.logo {
                            &.settings {
                                & path {
                                    fill: var(--accent-color);
                                }
                            }
                        }
                    }

                    &>.content {
                        display: none;
                        position: absolute;
                        width: 128px;
                        height: fit-content;
                        background-color: var(--color-background-mute);
                        right: 0;
                        z-index: 100;
                        border: 1px solid var(--color-text);
                        border-radius: 4px;
                        padding: 0 1rem;

                        &.show {
                            display: block;
                        }

                        & ul {
                            width: 100%;
                            height: 100%;
                            display: flex;
                            flex-direction: column;
                            align-items: center;

                            & li {
                                width: 100%;
                                min-width: auto;
                                max-width: none;
                                height: 60px;
                                min-height: auto;
                                max-height: none;

                                &:not(:first-child) {
                                    border-top: 1px solid var(--color-text);
                                }

                                & .switchThemeContainer {
                                    width: 88px;
                                    height: 44px;
                                    position: relative;
                                    border-radius: 50px;
                                    display: grid;
                                    grid-template-columns: 1fr 1fr;
                                    margin: 0 auto;
                                    padding: 5px 10px;
                                    background-color: var(--color-text);

                                    &:hover .switchOption::before {
                                        transform: rotate(90deg);
                                    }

                                    & .switchTheme {
                                        position: absolute;
                                        width: 100%;
                                        height: 100%;
                                        z-index: 10;
                                        opacity: 0;
                                        cursor: pointer;
                                    }

                                    & .switchOption {
                                        width: 34px;
                                        height: 34px;
                                        background-color: var(--color-background);
                                        border-radius: 50%;
                                        padding: 3px;

                                        transition: all ease 0.3s;
                                        transform: var(--theme-transform-option, none);

                                        &.dark::before {
                                            mask-image: url(../assets/moon.svg);
                                        }

                                        &::before {
                                            content: '';
                                            display: flex;
                                            background-color: var(--color-heading);
                                            mask-image: url(../assets/sun.svg);
                                            width: 28px;
                                            height: 28px;
                                            transition: all ease-in-out 0.3s;
                                        }
                                    }
                                }

                                &.switchLanguage {
                                    display: flex;
                                    justify-content: start;
                                    align-items: center;
                                    width: 100%;
                                    min-width: 88px;
                                    max-width: 88px;
                                    font-size: 1rem;

                                    &>* {
                                        cursor: pointer;
                                        height: 44px;
                                    }

                                    & input[value="Spanish"] {
                                        width: 20px;
                                        display: flex;
                                        justify-content: center;
                                        align-items: center;
                                        appearance: none;

                                        &::before {
                                            content: url(../assets/mexico-flag.png);
                                            width: 16px;
                                            height: 16px;
                                        }
                                    }

                                    & input[value="English"] {
                                        width: 20px;
                                        display: flex;
                                        justify-content: center;
                                        align-items: center;
                                        appearance: none;

                                        &::before {
                                            content: url(../assets/usa-flag.png);
                                            width: 16px;
                                            height: 16px;
                                        }
                                    }

                                    & label {
                                        display: flex;
                                        align-items: center;
                                        justify-content: center;
                                    }

                                    & :hover {
                                        color: var(--accent-color);
                                    }
                                }
                            }
                        }
                    }
                }
            }
        }
    }
}

li {
    list-style: none;
    padding: 0;
}

ul {
    padding: 0;
}

.logo {
    width: 32px;
    height: 32px;
    aspect-ratio: 1/1;
}
.logo.LinkedIn {
    & path, polygon {
        stroke: var(--color-heading);
    }
}
.logo.GitHub {
    & path {
        fill: var(--color-heading);
    }
}
.logo.settings {
    & path {
        fill: var(--color-heading);
    }
}
</style>