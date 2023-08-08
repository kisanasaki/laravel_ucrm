<script setup>
import { Link } from "@inertiajs/inertia-vue3";
</script>

<template>
    Inertiaテストです<br />
    <a href="/">aタグ</a><br />
    <Link href="/">Linkコンポーネント</Link><br />
    <Link :href="route('inertia.index')">InertiaController</Link><br />
</template>
