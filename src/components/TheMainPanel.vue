<template>
  <h1>{{ title }}</h1>
  <ul>
    <li v-for="holiday in holidays" :key="holiday.date">
      <p>{{ holiday.employee_id }}</p>
      <p>{{ holiday.date }}</p>
      <p>{{ holiday.comment }}</p>
    </li>
  </ul>
</template>

<script>
export default {
  props: ["title"],
  data() {
    return {
      holidays: [
        {
          employee_id: 1,
          date: "2020-10-01",
          comment: "Yaay! Vacation!",
        },
        {
          employee_id: 1,
          date: "2020-10-02",
          comment: "Yaay! Vacation!",
        },
        {
          employee_id: 1,
          date: "2020-10-03",
          comment: "Yaay! Vacation!",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  margin: auto;
  text-align: center;
  max-width: 600px;
  /* width: auto; */
}

li {
  list-style: none;
  border: black solid 1px;
  margin: auto;
  display: block;
  text-align: center;
  /* width: auto; */
}

li p {
  /* margin: auto; */
  display: block;
  text-align: center;
}
</style>
