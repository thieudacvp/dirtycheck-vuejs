<template>
    <form>
        <input v-model="form.first_name"/>
        <input v-model="form.last_name"/>
        <input v-model="form.email"/>
    </form> 
</template>

<script>
    const defaultForm = {
        first_name: '',
        last_name: '',
        email: '',
    }  
    export default {
      data () {
        return {
            form: defaultForm
        }
      },
      computed: {
        hasChanged () {
          return Object.keys(this.form).some(field => this.form[field] !== defaultForm[field]),
          console.log("changed")
        }
      }
    }
</script>