<template>
  <div>
    <div>
        <form>
            <label for="fname">First name:</label><br />
            <input type="text" id="fname" name="fname" v-model="firstname" /><br />
            <label for="lname">Last name:</label><br />
            <input type="text" id="lname" name="lname" v-model="lastname" /> <br />
            <input type="checkbox" id="vehicle1" name="vehicle1" v-model="checkbox">
            <label for="vehicle1"> I have a bike</label><br>
        </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
  },

  data() {
    return {
      firstname: null,
      lastname: null,
      checkbox: false,
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


