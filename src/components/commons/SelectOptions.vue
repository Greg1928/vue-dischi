<template>
    <select class="form-select" aria-label="Default select example" v-model="dataShared.SelectOption">
        <option value="All" selected="selected">All</option>
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
    width: 70%;
    display: flex;
    margin: auto;
}

</style>