<template>

  <b-container fluid class="mt-5">
    <b-row class="mx-auto" style="width:80%;">
      <div class="col-md-3 col-xs-12 order-md-2">
        <b-form-input v-model="text" placeholder="Search ..."></b-form-input>
      </div>
      <div class="col-md-9 col-xs-12 order-md-1 mx-auto details">
        <b-media>
          <img class="img-fluid float-md-left m-4" src="https://appexchangejp.salesforce.com/servlet/servlet.FileDownload?file=00P3A00000iaPg1UAE" width="200">
          <h1 class="mt-0">Audio Title</h1>
          <p class="mx-3 text-muted">
            2019-06-15
          </p>
          <p class="mx-3">
            テストテキスト
          </p>
          <b-button variant="success">再生する</b-button>
        </b-media>
      </div>
    </b-row>
    <b-row class="my-4 mx-auto" style="width:80%;">
      <b-col>
        <template>
          <div>
              <div>
                <b-table hover :items="items" :fields="fields"></b-table>
             </div>
          </div>
        </template>
      </b-col>
    </b-row>
    <nav class="navbar navbar-dark bg-dark navbar-fixed-bottom bottom-nav  text-white" role="navigation">
      <b-col cols="3">
        <b-media class="mt-2">
          <img class="player-img float-left mx-4" src="https://appexchangejp.salesforce.com/servlet/servlet.FileDownload?file=00P3A00000iaPg1UAE">
          <h4 class="mx-3">Audio Title</h4>
          <p class="mx-3 text-muted">
            2019-06-15
          </p>
        </b-media>
      </b-col>
      <b-col cols="6">
        <div class="button-group mb-3 text-center">
          <div class="btn-group" role="group" aria-label="Basic example">
            <button type="button" class="btn btn-secondary btn-lg">◀︎◀︎</button>
            <button type="button" class="btn btn-secondary btn-lg">▶︎</button>
            <button type="button" class="btn btn-secondary btn-lg">▶︎▶︎</button>
          </div>
        </div>
        <div class="player-group text-center">
          <b-row>
            <b-col>
              0:00
            </b-col>
            <b-col>
              <b-progress></b-progress>
            </b-col>
            <b-col>
            5:09
            </b-col>
          </b-row>
        </div>
      </b-col>
      <b-col class="text-center" cols="3">
       🔈
      </b-col>
    </nav>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      // Note 'isActive' is left out and will not appear in the rendered table
      fields: [
        {
          key: 'title',
          sortable: false
        },
        {
          key: 'time',
          sortable: false
        },
        {
          key: 'published_at',
          label: 'Person age',
          sortable: true
        }
      ],
      items: [
        { isActive: true, published_at: '2019/01/16', time: '3:00', title: 'タンバリンラジオ #1' },
        { isActive: false, published_at: '2019/02/02', time: '4:15', title: 'タンバリンラジオ #3' },
        { isActive: false, published_at: '2019/02/14', time: '3:51', title: 'タンバリンラジオ #2' },
        { isActive: true, published_at: '2019/03/04', time: '3:20', title: 'タンバリンラジオ #4' }
      ]
    }
  }
}
</script>

<style>
html { font-size: 1vw;}
@media screen and (max-width: 576px) {
  .details {
    text-align: center;
  }
}
.bottom-nav{
  width: 100%;
  height: 120px;
  position: absolute;
  bottom: 0;
  left:0;
}
.button-group{
  height: 50%;
}
.player-img {
width: 18%;
}
.player-group{
  height: 50%;
}
</style>
