<template>
  <section class="section__content">
    <div class="block block__left">
      <div class="block__left-text">
        <p>Образовательная платформа</p>
        <p>ХОД Future Academy</p>
        <p>Актуальные знания для новичков и профессионалов</p>
      </div>
      <img src="/src/assets/img/bg-left.svg" alt="" />
    </div>
    <div class="block block__right">
      <img src="/src/assets/img/devka.svg" alt="" />
    </div>
  </section>
</template>

<style lang="scss">
$block-width: 50%;
$text-color: white;
$font-weight-bold: 700;
$font-weight-regular: 500;
$line-height: 24px;
$margin-large: 40px;
$margin-small: 20px;

.section__content {
  display: flex;
  width: 100%;
  overflow: hidden;

  .block {
    position: relative;
    width: $block-width;

    &__left {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: flex-end;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

      &-text {
        position: absolute;
        color: $text-color;

        p {
          font-weight: $font-weight-bold;
          font-size: 36px;
          line-height: $line-height;
          display: flex;
          margin: $margin-large 16px;

          &:nth-child(3) {
            font-weight: $font-weight-regular;
            font-size: 20px;
            line-height: $line-height;
            opacity: 0.9;
          }
        }
      }
    }

    &__right {
      position: relative;

      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
  }
}

@media (max-width: 1198px) {
  .section__content {
    display: flex;
    flex-direction: column-reverse;

    .block {
      width: 100%;
      height: 220px;

      &__left {
        display: flex;
        align-items: center;
        justify-content: flex-start;

        &-text {
          display: flex;
          flex-direction: column;
          color: $text-color;
          width: 100%;
          text-align: left;

          p {
            font-weight: $font-weight-bold;
            font-size: 18px;
            line-height: $line-height;
            margin: $margin-small;
            display: block;

            &:nth-child(3) {
              font-size: 16px;
            }
          }
        }
      }
    }
  }
}
</style>
