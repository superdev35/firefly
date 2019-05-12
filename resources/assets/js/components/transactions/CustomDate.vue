<template>
    <div class="form-group">
        <div class="col-sm-12 text-sm">
            {{ title }}
        </div>
        <div class="col-sm-12">
            <input type="date" class="form-control" :name="name"
                   :title="title" autocomplete="off"
                   ref="date"
                   :value="value" @input="handleInput"
                   :placeholder="title">
        </div>
    </div>
</template>

<script>
    export default {
        name: "CustomDate",
        props: {
            value: String,
            title: String,
            name: String
        },
        methods: {
            handleInput(e) {
                this.$emit('input', this.$refs.date.value);
            }
        }
    }
</script>

<style scoped>

</style>