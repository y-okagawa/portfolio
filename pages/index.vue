<template>
  <div class="container">
    <!-- Header -->
    <header id="header">
      <div class="inner">
        <a href="#" class="image avatar"
          ><img src="~/assets/images/avatar.png" alt=""
        /></a>
        <h1>
          <strong>I am Yuya Okagawa.</strong><br />
          I work as an Web Development Engineer.
        </h1>
      </div>
    </header>

    <!-- Main -->
    <div id="main">
      <!-- One -->
      <section id="one">
        <header class="major">
          <h2>
            Profile
          </h2>
        </header>
        <p>
          サーバサイドの領域を得意とし、PHPでのWEBアプリケーション開発経験が豊富。加えてフロントエンド、インフラの一通りの構築が可能。<br />
          また、スクラムを用いたアジャイル開発にも取り組んでおり、スクラムマスターとしてWEBアプリケーションの開発に奮闘中。<br />
          最近の一番の関心ごとは「変更に強いソフトウェア」にするための開発、チームビルディング。
        </p>
      </section>

      <!-- Two -->
      <section id="two">
        <h2>Main Skills</h2>
        <div class="row">
          <div class="col-12">
            <ul class="skills">
              <li class="skill">
                <span class="bar percent_80"></span>
                <p class="name">CakePHP2系</p>
              </li>
              <li class="skill">
                <span class="bar percent_70"></span>
                <p class="name">Laravel</p>
              </li>
              <li class="skill">
                <span class="bar percent_40"></span>
                <p class="name">Vue.js / Nuxt.js</p>
              </li>
              <li class="skill">
                <span class="bar percent_80"></span>
                <p class="name">AWS</p>
              </li>
              <li class="skill">
                <span class="bar percent_60"></span>
                <p class="name">スクラムマスター</p>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <!-- blog -->
      <section id="blog">
        <h2>blog</h2>
        <div class="row blogs">
          <article class="col-6 col-12-xsmall blog">
            <a class="title fit" style="cursor: pointer; outline: 0px;">
              hoge
            </a>
          </article>
        </div>
      </section>

      <section>
        <h2>Certificate</h2>
        <ul>
          <li>Scrum Inc.認定スクラムマスター（LSM）</li>
          <li>応用情報技術者</li>
          <li>日商簿記2級</li>
        </ul>
      </section>

      <!-- Three -->
      <section id="three">
        <h2>Contact me</h2>
        <p>
          TwitterのDMからご連絡ください。<br />
          <a href="https://twitter.com/okagaway" class="icon brands fa-twitter"
            >@okagaway<span class="label">Twitter</span></a
          >
        </p>
      </section>
    </div>
    <!-- Footer -->
    <footer id="footer">
      <div class="inner">
        <ul class="icons">
          <li>
            <a
              href="https://twitter.com/okagaway"
              class="icon brands fa-twitter"
              ><span class="label">Twitter</span></a
            >
          </li>
          <li>
            <a href="https://github.com/y-okagawa" class="icon brands fa-github"
              ><span class="label">Github</span></a
            >
          </li>
        </ul>
        <ul class="copyright">
          <li>Design: <a href="http://html5up.net">HTML5 UP</a></li>
        </ul>
      </div>
    </footer>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~assets/sass/libs/_vendor.scss';
.blog {
  margin: 0 0 2em 0;
  display: inline-grid;
  .title {
    border-radius: _size(border-radius);
    border: 0;
    display: inline-block;
    position: relative;

    &:before {
      @include vendor(
        'transition',
        'opacity #{_duration(transition)} ease-in-out'
      );
      background: url('~assets/images/overlay.png');
      border-radius: _size(border-radius);
      content: '';
      display: block;
      height: 100%;
      left: 0;
      opacity: 0.5;
      position: absolute;
      top: 0;
      width: 100%;
    }

    &.thumb {
      text-align: center;

      &:after {
        @include vendor(
          'transition',
          'opacity #{_duration(transition)} ease-in-out'
        );
        border-radius: _size(border-radius);
        border: solid 3px rgba(255, 255, 255, 0.5);
        color: #fff;
        content: 'View';
        display: inline-block;
        font-size: 0.8em;
        font-weight: _font(weight-bold);
        left: 50%;
        line-height: 2.25em;
        margin: -1.25em 0 0 -3em;
        opacity: 0;
        padding: 0 1.5em;
        position: absolute;
        text-align: center;
        text-decoration: none;
        top: 50%;
        white-space: nowrap;
      }

      &:hover {
        &:after {
          opacity: 1;
        }

        &:before {
          background: url('~assets/images/overlay.png'),
            url('~assets/images/overlay.png');
          opacity: 1;
        }
      }
    }
  }
}

.skills {
  list-style: none;
  padding: 0;

  .skill {
    height: 30px;
    margin-bottom: 20px;
    background-color: #efefef;
    position: relative;

    .bar {
      position: absolute;
      top: 0;
      left: 0;
      height: 30px;
      display: inline-block;
      background-color: #ab9e96;
      $rate: 10;
      @for $i from 1 through 10 {
        &.percent_#{$rate*$i} {
          width: #{1% * $rate * $i};
        }
      }
    }

    .name {
      position: absolute;
      left: 0;
      color: #ffffff;
      margin-left: 10px;
    }
  }
}
</style>
