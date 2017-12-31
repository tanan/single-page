<template lang="pug">
.page
  header.header
    p.site-title-sub Web designer's portfolio
    h1.site-title HI, MY NAME IS...
    p.site-description Check out some of my works
    .buttons
      a.button(href="#about") LEARN MORE
      a.button.button-showy(href="#contact") SEND MESSAGE
  section.about(id="about")
    h2.heading ABOUT ME
    p.about-text 初めまして、日本でWebデザイナーをしています
      br
      | KCCSという会社を退職し、ユーザベースで働いています。
      br
      | よろしくお願いします.
    p.about-text 初めまして、日本でWebデザイナーをしています
      br
      | KCCSという会社を退職し、ユーザベースで働いています。
      br
      | 実践的なコーディングをします
  section.works
    h2.heading WORKS
    .works-wrapper
      .work-box.tree
        img.work-image(src="../assets/images/tree.jpg" alt="制作事例1")
        .work-description
          .work-description-inner
            p.work-text 一つ目の制作事例が入ります。
              br
              | 簡単な説明が入ります
              br
              | 使用ツール: XXX, XXX, XXX
              br
              a.button.button-ghost(href="#") READ MORE
      .work-box.building
        img.work-image(src="../assets/images/building.jpg" alt="制作事例1")
        .work-description
          .work-description-inner
            p.work-text 一つ目の制作事例が入ります。
              br
              | 簡単な説明が入ります
              br
              | 使用ツール: XXX, XXX, XXX
              br
              a.button.button-ghost(href="#") READ MORE
      .work-box.lake
        img.work-image(src="../assets/images/lake.jpg" alt="制作事例1")
        .work-description
          .work-description-inner
            p.work-text 一つ目の制作事例が入ります。
              br
              | 簡単な説明が入ります
              br
              | 使用ツール: XXX, XXX, XXX
              br
              a.button.button-ghost(href="#") READ MORE
      .work-box.sky
        img.work-image(src="../assets/images/sky.jpg" alt="制作事例1")
        .work-description
          .work-description-inner
            p.work-text 一つ目の制作事例が入ります。
              br
              | 簡単な説明が入ります
              br
              | 使用ツール: XXX, XXX, XXX
              br
              a.button.button-ghost(href="#") READ MORE
  section.skills
  section.contact(id="contact")
  footer.footer
</template>

<script>
</script>

<style scoped lang="scss">

.header {
  padding: 170px 30px 80px;
  .site-title-sub {
    margin: 0 0 30px;
    letter-spacing: 1px;
    font-size: 2.2rem;
  }
  .site-title-sub::before,
  .site-title-sub::after {
    content: '';
    display: inline-block;
    width: 140px;
    height: 2px;
    margin: 0 30px;
    background-color: #fff;
    vertical-align: middle;
  }
  .site-title {
    margin: 50px 0 40px;
    font-size: 7.6rem;
  }
  .site-description {
    margin-bottom: 50px;
    color: #888;
    font-size: 1.6rem;
  }
}

.about {
    padding: 80px 30px;
    background-color: #fff;
    color: #333;
    &::before {
        bottom: 5px;
    }
    .about-text {
        margin: 30px 0;
        line-height: 2.5;
    }
}

.works {
    background-color: #383634;
    padding: 80px 0;
    .works-wrapper {
        display: table;
        width: 100%;
        margin-top: 60px;
        table-layout: fixed;
        .work-box {
            position: relative;
            display: table-cell;
            &::after {
                content: '';
                position: absolute;
                top: 50%;
                left: 0;
                width: 100%;
                height: 50%;
                background: no-repeat;
                background-size: 100% 100%;
                opacity: .2;
                transform: scaleY(-1);
            }
            &.tree::after {
              background-image: url('../assets/images/tree.jpg');
            }
            &.building::after {
              background-image: url('../assets/images/building.jpg');
            }
            &.lake::after {
              background-image: url('../assets/images/lake.jpg');
            }
            &.sky::after {
              background-image: url('../assets/images/sky.jpg');
            }
            &:nth-child(odd) .work-image {
              margin: 60% 0 0;
            }
            &:nth-child(odd) .work-description,
            &:nth-child(odd)::after {
              top: 0;
            }

            .work-description {
                position: absolute;
                top: 50%;
                left: 0;
                width: 100%;
                height: 50%;
                z-index: 1;
                overflow-y: auto;
                .work-description-inner {
                  display: table;
                  width: 100%;
                  height: 100%;
                  padding: 20px;
                  .work-text {
                    display: table-cell;
                    vertical-align: middle;
                    font-size: 1.2rem;
                    line-height: 2;
                  }
                  .work-text .button {
                    width: 60%;
                    margin-top: 20px;
                    padding: 3px;
                  }
                }
            }
            .work-image {
                display: block;
                width: 100%;
                margin: 0 0 60%;
            }
        }
    }
}
</style>