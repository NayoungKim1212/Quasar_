<template>
    <div>
        <div class="text-h4">Mypage</div>
        <q-layout>
            <ul>
                <li>
                    <router-link to="/profile">Profile</router-link>
                </li>
                <li>
                    <router-link to="/password">Password</router-link>
                </li>
                <li>
                    <router-link to="/bookmark">Bookmark</router-link>
                </li>
            </ul>
            <q-page-container>
                <router-view />
            </q-page-container>
        </q-layout>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>