<script setup></script>
<template>


    <div>
        <input type="text"
        class="form-control"
        :name="name"
        :type="type"
        :placeholder="placeholder"
        :value="modelValue"
        @input="$emit('update:modelValue')">
    </div>
    <ul v-if="errors.length" class="errors-list">
        <li v-for="error in errors">{{ error }}</li>
    </ul>
</template>
<style></style>

