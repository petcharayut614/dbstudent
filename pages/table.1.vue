<template>
<div>
  <v-data-table
    :headers="headers"
    :items="desserts"
    class="elevation-1"
  >
    <template slot="items" slot-scope="props">
      <td>{{ props.item.b_id }}</td>
      <td class="text-xs-center">{{ props.item.b_name }}</td>
      <td class="text-xs-center">{{ props.item.b_group }}</td>
      <td class="text-xs-center">{{ props.item.b_price }}</td>

    </template>
    <template slot="pageText" slot-scope="props">
    Lignes {{ props.pageStart }} - {{ props.pageStop }} de {{ props.itemsLength }}
    </template>
  </v-data-table>
  <div>
    <v-btn color="brown lighten-1">แก้ไขข้อมูล</v-btn>
    <v-btn color="brown lighten-1">เพิ่มข้อมูล</v-btn>
    <v-btn color="error">ลบ</v-btn>
  </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      headers: [
        {
          text: "B_ID",
          align: "left",
          sortable: false,
          value: "name"
        },
        { text: "B_Name", value: "B_Name", align: "center" },
        { text: "B_Group", value: "B_Group", align: "center" },
        { text: "B_Price", value: "B_Price", align: "center" }
      ],
      desserts: []
    };
  },
  async created() {
    this.getstudent();
  },
  methods: {
    async getstudent() {
      let res = await this.$http.get(
        "http://127.0.0.1/php-test1/list-book.php"
      );
      this.desserts = res.data.student;
    }
  }
};
</script>