<template>
    <div
        id="filter-bar-dropdown-component"
        class="border border-gray-600"
        :style="`width: ${row * 200}px`"
    >
        <ul class="flex flex-wrap">
            <li
                class="flex-none cursor-pointer hover:bg-gray-200"
                v-for="(option, index) in options"
                :key="index"
                :style="`width: ${100 / row}%`"
            >
                <p @click="filter(option)" class="flex justify-start p-4">
                    {{ option }}
                </p>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: {
        options: {
            type: Array,
            default: function() {
                return null;
            }
        },
        row: {
            type: Number,
            default: 1
        }
    },
    methods: {
        filter(option) {
            this.$emit('filtering', option);
        }
    }
};
</script>

<style lang="scss" scoped>
#filter-bar-dropdown-component {
    max-height: 400px;
    overflow: scroll;
}
</style>
