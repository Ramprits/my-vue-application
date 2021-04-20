<template>
  <div v-for="employee in filteredEmployees" :key="employee.id">
    <div @click="getEmployee(employee)">
      {{ employee.first_name }} - {{ employee.last_name }}
      <a class="is-link is-block">{{ employee.email }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",

  data() {
    return {
      employees: [
        {
          id: 1,
          first_name: "Carlie",
          last_name: "McGeouch",
          email: "cmcgeouch0@hatena.ne.jp",
          gender: "Male",
          ip_address: "93.165.139.202",
        },
        {
          id: 2,
          first_name: "Jaquenette",
          last_name: "Boggon",
          email: "jboggon1@clickbank.net",
          gender: "Agender",
          ip_address: "20.9.3.43",
        },
        {
          id: 3,
          first_name: "Kimberley",
          last_name: "De Ath",
          email: "kdeath2@sciencedaily.com",
          gender: "Male",
          ip_address: "13.121.29.18",
        },
        {
          id: 4,
          first_name: "Remy",
          last_name: "Bodemeaid",
          email: "rbodemeaid3@google.nl",
          gender: "Bigender",
          ip_address: "148.237.253.70",
        },
        {
          id: 5,
          first_name: "Prentiss",
          last_name: "Burk",
          email: "pburk4@cisco.com",
          gender: "Female",
          ip_address: "206.164.164.69",
        },
        {
          id: 6,
          first_name: "Stefa",
          last_name: "Goodey",
          email: "sgoodey5@chronoengine.com",
          gender: "Female",
          ip_address: "56.254.126.149",
        },
        {
          id: 7,
          first_name: "Christie",
          last_name: "Cuskery",
          email: "ccuskery6@tamu.edu",
          gender: "Non-binary",
          ip_address: "104.97.158.56",
        },
        {
          id: 8,
          first_name: "Nicolas",
          last_name: "Clinkard",
          email: "nclinkard7@biglobe.ne.jp",
          gender: "Genderqueer",
          ip_address: "172.73.138.102",
        },
        {
          id: 9,
          first_name: "Alicia",
          last_name: "Poyser",
          email: "apoyser8@apache.org",
          gender: "Male",
          ip_address: "143.22.45.201",
        },
        {
          id: 10,
          first_name: "Roz",
          last_name: "Teale",
          email: "rteale9@samsung.com",
          gender: "Bigender",
          ip_address: "53.178.124.122",
        },
      ],
    };
  },
  methods: {
    onMouseOver(e, name) {
      console.log("Event", name);
    },
    getEmployee(employee) {
      this.filteredName == employee.first_name;
    },
  },
  computed: {
    filteredEmployees() {
      return this.employees.filter(
        (employee) => employee.first_name == "Christie"
      );
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 10px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
