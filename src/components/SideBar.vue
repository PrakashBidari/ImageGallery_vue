<script setup>
import { defineEmits } from 'vue';
const emits = defineEmits(['selectOption']);

const selectOption = (isColor)=>{
    emits("selectOption",isColor);
}

</script>


<template>
    <VNavigationDrawer expand-on-hover rail>
        <v-list>
            <v-list-item prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg" title="Prakash Bidari"
                subtitle="123@cmail.com"></v-list-item>
        </v-list>

        <VDivider />
        <VList density="compact">
            <VListItem prepend-icon="mdi-image" title="Color Gallery" value="color" @click="selectOption(true)" />
            <VListItem prepend-icon="mdi-dialpad" title="Gray Space Gallery" value="color" @click="selectOption(false)" />
        </VList>

    </VNavigationDrawer>
</template>