<template>
    <div v-if="lang_tag === 'HTML'" class="tag">
        <img alt="svgImg" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciICB2aWV3Qm94PSIwIDAgNDggNDgiIHdpZHRoPSI0OHB4IiBoZWlnaHQ9IjQ4cHgiPjxwYXRoIGZpbGw9IiNFNjUxMDAiIGQ9Ik00MSw1SDdsMywzNGwxNCw0bDE0LTRMNDEsNUw0MSw1eiIvPjxwYXRoIGZpbGw9IiNGRjZEMDAiIGQ9Ik0yNCA4TDI0IDM5LjkgMzUuMiAzNi43IDM3LjcgOHoiLz48cGF0aCBmaWxsPSIjRkZGIiBkPSJNMjQsMjV2LTRoOC42bC0wLjcsMTEuNUwyNCwzNS4xdi00LjJsNC4xLTEuNGwwLjMtNC41SDI0eiBNMzIuOSwxN2wwLjMtNEgyNHY0SDMyLjl6Ii8+PHBhdGggZmlsbD0iI0VFRSIgZD0iTTI0LDMwLjl2NC4ybC03LjktMi42TDE1LjcsMjdoNGwwLjIsMi41TDI0LDMwLjl6IE0xOS4xLDE3SDI0di00aC05LjFsMC43LDEySDI0di00aC00LjZMMTkuMSwxN3oiLz48L3N2Zz4="/>HTML
    </div>
    <div v-else-if="lang_tag === 'CSS'" class="tag">
        <img alt="svgImg" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciICB2aWV3Qm94PSIwIDAgNDggNDgiIHdpZHRoPSI0OHB4IiBoZWlnaHQ9IjQ4cHgiPjxwYXRoIGZpbGw9IiMwMjc3QkQiIGQ9Ik00MSw1SDdsMywzNGwxNCw0bDE0LTRMNDEsNUw0MSw1eiIvPjxwYXRoIGZpbGw9IiMwMzlCRTUiIGQ9Ik0yNCA4TDI0IDM5LjkgMzUuMiAzNi43IDM3LjcgOHoiLz48cGF0aCBmaWxsPSIjRkZGIiBkPSJNMzMuMSAxM0wyNCAxMyAyNCAxNyAyOC45IDE3IDI4LjYgMjEgMjQgMjEgMjQgMjUgMjguNCAyNSAyOC4xIDI5LjUgMjQgMzAuOSAyNCAzNS4xIDMxLjkgMzIuNSAzMi42IDIxIDMyLjYgMjF6Ii8+PHBhdGggZmlsbD0iI0VFRSIgZD0iTTI0LDEzdjRoLTguOWwtMC4zLTRIMjR6IE0xOS40LDIxbDAuMiw0SDI0di00SDE5LjR6IE0xOS44LDI3aC00bDAuMyw1LjVsNy45LDIuNnYtNC4ybC00LjEtMS40TDE5LjgsMjd6Ii8+PC9zdmc+"/>CSS
    </div>
    <div v-else-if="lang_tag === 'JS'" class="tag">
        <img alt="svgImg" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciICB2aWV3Qm94PSIwIDAgNDggNDgiIHdpZHRoPSI0OHB4IiBoZWlnaHQ9IjQ4cHgiPjxwYXRoIGZpbGw9IiNmZmQ2MDAiIGQ9Ik02LDQyVjZoMzZ2MzZINnoiLz48cGF0aCBmaWxsPSIjMDAwMDAxIiBkPSJNMjkuNTM4IDMyLjk0N2MuNjkyIDEuMTI0IDEuNDQ0IDIuMjAxIDMuMDM3IDIuMjAxIDEuMzM4IDAgMi4wNC0uNjY1IDIuMDQtMS41ODUgMC0xLjEwMS0uNzI2LTEuNDkyLTIuMTk4LTIuMTMzbC0uODA3LS4zNDRjLTIuMzI5LS45ODgtMy44NzgtMi4yMjYtMy44NzgtNC44NDEgMC0yLjQxIDEuODQ1LTQuMjQ0IDQuNzI4LTQuMjQ0IDIuMDUzIDAgMy41MjguNzExIDQuNTkyIDIuNTczbC0yLjUxNCAxLjYwN2MtLjU1My0uOTg4LTEuMTUxLTEuMzc3LTIuMDc4LTEuMzc3LS45NDYgMC0xLjU0NS41OTctMS41NDUgMS4zNzcgMCAuOTY0LjYgMS4zNTQgMS45ODUgMS45NTFsLjgwNy4zNDRDMzYuNDUyIDI5LjY0NSAzOCAzMC44MzkgMzggMzMuNTIzIDM4IDM2LjQxNSAzNS43MTYgMzggMzIuNjUgMzhjLTIuOTk5IDAtNC43MDItMS41MDUtNS42NS0zLjM2OEwyOS41MzggMzIuOTQ3ek0xNy45NTIgMzMuMDI5Yy41MDYuOTA2IDEuMjc1IDEuNjAzIDIuMzgxIDEuNjAzIDEuMDU4IDAgMS42NjctLjQxOCAxLjY2Ny0yLjA0M1YyMmgzLjMzM3YxMS4xMDFjMCAzLjM2Ny0xLjk1MyA0Ljg5OS00LjgwNSA0Ljg5OS0yLjU3NyAwLTQuNDM3LTEuNzQ2LTUuMTk1LTMuMzY4TDE3Ljk1MiAzMy4wMjl6Ii8+PC9zdmc+"/>JavaScript
    </div>
    <div v-else-if="lang_tag === 'VUE'" class="tag">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 261.76 226.69"><path d="M161.096.001l-30.225 52.351L100.647.001H-.005l130.877 226.688L261.749.001z" fill="#41b883"/><path d="M161.096.001l-30.225 52.351L100.647.001H52.346l78.526 136.01L209.398.001z" fill="#34495e"/></svg>VueJS
    </div>
</template>

<script setup>
const props = defineProps(["lang_tag"])
</script>

<style scoped>
    div.tag {
        display: flex;
        flex-direction: row;
        align-items: center;

        &>img {
            width: 2rem;
            height: 2rem;
            margin: 0 0.25rem 0 0;
        }

        &>svg {
            width: 2rem;
            height: 2rem;
            margin: 0 0.25rem 0 0;
        }
    }
</style>