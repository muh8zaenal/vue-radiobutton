<template>
    <div>
        <table>
            <tr>
                <td>Name </td>
                <td>
                    <input type="text" v-model="fullname">
                </td>
            </tr>
            <tr>
                <td>Birth Date </td>
                <td>
                    <input type="date" v-model="birthDate">
                </td>
            </tr>
        </table>
        
        <br>
        
    </div>
</template>
<script>
export default {
    data(){
        return{
            fullname:'',
            birthDate: '',
        }
    }
}
</script>
<style scoped>
input {
margin-bottom: 5px;
}
input[type=date]{
    padding: 8px;
}
</style>