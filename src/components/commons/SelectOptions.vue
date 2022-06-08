<template>
    <select class="form-select" aria-label="Default select example" v-model="dataShared.SelectOption">
        <option value="All" selected="selected">Browse All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
    </select>
</template>

<script>
import dataShared from '../../shared/dataShared';

export default {
    name: 'SelectOptions',
    data(){
        return{
            dataShared
        }
    }
}
</script>

<style lang="scss" scoped>
select{
    width: 13%;
    color: var(--secondary-color);
    text-transform: uppercase;
    cursor: pointer;
    font-weight: bold;
    margin: auto;
}

</style>