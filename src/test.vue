<template>
    <div v-for="(item, index) in items">
        <div>{{ item.name }}</div>
        <div>{{ item.value }}</div>
        <div>{{ formatIndex(index) }}</div>
    </div>
</template>

<script lang="ts" >
import { defineComponent } from 'vue';  

type Data = {
  name: string;
  value: number;
}

export default defineComponent({
    name: "test",

    setup() {
        const items: Data[] = [{ name: 'One', value: 1 }];
        
        function formatIndex(index: number): string {
            return `No ${index + 1}`;
        }

        return {
            items,
            formatIndex
        }
    }
})
</script>