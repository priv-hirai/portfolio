<template>
  <header>
    <div class="header">
      <div class="ly_inner header_inner">
        <p>
          <a href="/">アイコン</a>
        </p>
        <nav id="nav-global">
          <div class="nav_wrap">
            <div>
              <ul class="menu">
                <li><a href="#profile">profile</a></li>
                <li><a href="#skill">skill</a></li>
              </ul>
            </div>
          </div>
        </nav>
        <p class="date">
          <span class="year">{{year}}</span>
          <span class="month_day">{{date}}</span>
        </p>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  name: 'header',
  data() {
    return {
      year : null,
      date : null,
    }
  },
  created: function() {
    // ヘッダーに今日の日付をセットする
    this.getToday();
  },
  methods: {
    getToday: function() {
      console.log('getToday');
      let newDate = new Date();
      // 今年の年数取得
      let newDateYear = newDate.getFullYear();
      // 今日の月数取得
      let newDateMonth = this.convertZeroPadding(newDate.getMonth()+1);
      // 今日の日付取得
      let newDateDay = this.convertZeroPadding(newDate.getDate());
      // 年セット
      this.year = newDateYear + ".";
      // 今日の日付セット
      this.date = String(newDateMonth) + "." + String(newDateDay);
    },
    convertZeroPadding: function(date){
      console.log("convertZeroPadding");
      // 1桁の数値なら0埋めする
      if (date.toString().length == 1){
        date = "0" + String(date);
      }

      return date;
    }
  }
}
</script>
<style scoped>

</style>
