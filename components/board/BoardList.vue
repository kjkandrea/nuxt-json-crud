<template>
  <div>
    <v-data-table
      :headers="headers"
      :items="tables"
      :page.sync="page"
      :items-per-page="itemsPerPage"
      hide-default-footer
      class="elevation-1"
      @page-count="pageCount = $event"
    ></v-data-table>
    <div class="text-center pt-2">
      <v-pagination v-model="page" :length="pageCount"></v-pagination>
      <!-- <v-text-field
        :value="itemsPerPage"
        label="Items per page"
        type="number"
        min="5"
        max="15"
        @input="itemsPerPage = parseInt($event, 10)"
      ></v-text-field> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "BoardList",
  data () {
    return {
      page: 1,
      pageCount: 0,
      itemsPerPage: 5,
      headers: [
        { text: 'ID', value: 'id' },
        {
          text: '주제',
          align: 'start',
          sortable: false,
          value: 'title',
        },
        { text: '작성자', value: 'author' },
        { text: '작성일', value: 'date' },
      ],
      tables: [
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        },
        {
          id : '1',
          title: 'Frozen Yogurt',
          author: '멈무',
          date: '2018-03-28'
        }
      ],
    }
  },
}
</script>