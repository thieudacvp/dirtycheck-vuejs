<template>
  <div>
    <div>
        <form>
            <label for="fname">First name:</label><br />
            <input type="text" id="fname" name="fname" v-model="firstname" /><br />
            <label for="lname">Last name:</label><br />
            <input type="text" id="lname" name="lname" v-model="lastname" />
        </form>
    </div>
    <!-- <div>
            <form-1/>
    </div> -->
  </div>
</template>

<script>
//import form1 from './components/Form.vue'
export default {
  name: "App",
  components: {
//      form1
  },

  data() {
    return {
      firstname: null,
      lastname: null,
      dirtycheck: false,
    };
  },
  methods: {},
  
  updated() {
      window.onbeforeunload = function (event) {
        var message =
          "Important: Please click on 'Save' button to leave this page.";           
        if (typeof event == "undefined") {
          event = window.event;
        }
        if (event) {
          event.returnValue = message;
        }
        return message;
      };
  },
};
</script>


