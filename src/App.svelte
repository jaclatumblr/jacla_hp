<script>
  import { onMount } from 'svelte';

  let events = [];

  // onMount内に関数を追加
  onMount(() => {
    // ここにカルーセルデータを追加する
  });
</script>

<style>
  body {
    background-color: #1F1F1F !important;
    margin: 0;
    height: 100%;
    padding: 0;
  }

  /* カスタムスタイルをここに追加 */
  .hero {
    background-image: url('/path/to/your/hero-image.jpg');
    background-size: cover;
    background-position: center;
    color: white;
    text-align: center;
    padding: 5rem 1rem;
  }

  .carousel img {
    width: 100%;
    height: auto;
  }
</style>

<div class="container">
  <!-- ロゴとナビゲーションバー -->
  <nav class="navbar">
    <div class="navbar-brand">
      <a class="navbar-item" href="/">
        <img src="/path/to/logo.png" alt="ロゴ" id="logo">
      </a>
    </div>
    <div class="navbar-menu">
      <div class="navbar-end">
        <a class="navbar-item" href="#info">Information</a>
        <a class="navbar-item" href="#about">活動概要</a>
        <a class="navbar-item" href="#schedule">活動予定</a>
        <a class="navbar-item" href="#equipment">機材紹介</a>
        <a class="navbar-item" href="#contact">お問い合わせ</a>
      </div>
    </div>
  </nav>
  
  <!-- ヒーローセクション -->
  <section class="hero">
    <div class="hero-body">
      <h1 class="title">What is Jacla?</h1>
      <p class="subtitle">
        ジャズからロックまで
      </p>
    </div>
  </section>
  
  <!-- Information -->
  <section class="section" id="info">
    <div class="container">
      <h2 class="title">Information</h2>
      <!-- 更新履歴を記述 -->
      <p>ここに更新履歴が表示</p>
    </div>
  </section>
  
  <!-- 活動概要 -->
  <section class="section" id="about">
    <div class="container">
      <h2 class="title">活動概要</h2>
      <p>ここにサークルの活動内容を記述</p>
    </div>
  </section>
  
  <!-- 活動予定 -->
  <section class="section" id="schedule">
    <div class="container">
      <h2 class="title">活動予定</h2>
      <!-- Bulmaカレンダー? -->
      <div class="calendar">
        <table class="table is-fullwidth">
          <thead>
            <tr>
              <th>Month/Year</th>
              <th>Day</th>
              <th>Event</th>
            </tr>
          </thead>
          <tbody>
            {#each events as event}
              <tr>
                <td>{event.month}/{event.year}</td>
                <td>{event.day}</td>
                <td>{event.description}</td>
              </tr>
            {/each}
          </tbody>
        </table>
      </div>
    </div>
  </section>
  
  <!-- 機材紹介 -->
  <section class="section" id="equipment">
    <div class="container">
      <h2 class="title">機材紹介</h2>
      <!-- カルーセル -->
      <div class="carousel">
        <div class="carousel-item">
          <img src="/path/to/equipment1.jpg" alt="アンプ">
          <p>アンプの説明</p>
        </div>
        <!-- これ以降カルーセルのアイテムを追加 -->
      </div>
    </div>
  </section>

  <!-- お問い合わせ -->
  <section class="section" id="contact">
    <div class="container">
      <h2 class="title">お問い合わせ</h2>
      <p>ここに問い合わせ情報を記述</p>
    </div>
  </section>
</div>