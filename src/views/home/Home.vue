<template>
  <div class="home-root">
    <div class="home-display">
      <div id="observe-star-container" class="display-star"></div>
    </div>
    <div class="home-main">
      <div class="main-content">
        <div class="content-item">
          <div class="item-image">
            <img src="@/assets/images/bg.jpg" alt="">
          </div>
          <div class="item-detail">
            <div class="detail-date">十一月 03, 2020</div>
            <div class="detail-title">送给自己的生日礼物</div>
            <div class="detail-describe">我们每个人都是一个人，即使短暂的时刻有人陪在你身边，对方也终究会离去。因为生命最终的目的地就是孤寂，这种孤寂并不能靠恋爱，友谊，亲情</div>
          </div>
        </div>
        <div class="content-item">
          <div class="item-image">
            <img src="@/assets/images/bg.jpg" alt="">
          </div>
          <div class="item-detail">
            <div class="detail-date">十一月 03, 2020</div>
            <div class="detail-title">送给自己的生日礼物</div>
            <div class="detail-describe">我们每个人都是一个人，即使短暂的时刻有人陪在你身边，对方也终究会离去。因为生命最终的目的地就是孤寂，这种孤寂并不能靠恋爱，友谊，亲情</div>
          </div>
        </div>
        <div class="content-item">
          <div class="item-image">
            <img src="@/assets/images/bg.jpg" alt="">
          </div>
          <div class="item-detail">
            <div class="detail-date">十一月 03, 2020</div>
            <div class="detail-title">送给自己的生日礼物</div>
            <div class="detail-describe">我们每个人都是一个人，即使短暂的时刻有人陪在你身边，对方也终究会离去。因为生命最终的目的地就是孤寂，这种孤寂并不能靠恋爱，友谊，亲情</div>
          </div>
        </div>
        <div class="content-item">
          <div class="item-image">
            <img src="@/assets/images/bg.jpg" alt="">
          </div>
          <div class="item-detail">
            <div class="detail-date">十一月 03, 2020</div>
            <div class="detail-title">送给自己的生日礼物</div>
            <div class="detail-describe">我们每个人都是一个人，即使短暂的时刻有人陪在你身边，对方也终究会离去。因为生命最终的目的地就是孤寂，这种孤寂并不能靠恋爱，友谊，亲情</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {

    }
  }
}
</script>

<style lang="less" scoped>
.home-root {
  &::before {
    content: '';
    position: fixed;
    top: 0;
    left: 50%;
    z-index: -1;
    width: 1px;
    height: 100%;
    background: #ebebeb;
    transform: translateX(-50%);
  }

  .home-display {
    overflow: hidden;
    width: 100%;
    height: 100vh;
    background-image: url(~@/assets/images/bg.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;

    .display-star {
      width: 100%;
      height: 100%;
    }
  }
  .home-main {

    .main-content {
      width: 1200px;
      margin: 0 auto;
      transition: all .3s;

      .content-item {
        position: relative;
        margin-top: 100px;
        font-size: 0;

        &:nth-child(odd) {
          text-align: left;

          .item-detail {
            left: 660px;
          }
        }

        &:nth-child(even) {
          text-align: right;

          .item-detail {
            right: 660px;
          }
        }

        .item-image {
          display: inline-block;
          position: relative;
          overflow: hidden;
          z-index: 1;
          width: 680px;
          height: 440px;
          background: red;
          border-radius: 6px;
          cursor: pointer;

          img {
            width: 100%;
            height: 100%;
          }
        }

        .item-detail {
          position: absolute;
          top: 20px;
          width: 500px;
          height: 400px;
          padding: 80px 100px 0 80px;
          border: 1px solid #ebebeb;
          text-align: left;
          background-color: #ffffff;
          border-radius: 6px;
          box-sizing: border-box;

          .detail-date {
            font-size: 12px;
            color: #999999;
          }

          .detail-title {
            margin-top: 8px;
            line-height: 25px;
            font-size: 24px;
          }

          .detail-describe {
            margin-top: 10px;
            line-height: 22px;
            font-size: 14px;
            color: #666666;
          }
        }
      }
    }

    @media screen and (max-width: 1200px) {
      .main-content {
        width: 900px;

        .content-item {
          &:nth-child(odd) {
            .item-detail {
              left: 450px;
            }
          }

          &:nth-child(even) {
            .item-detail {
              right: 450px;
            }
          }

          .item-image {
            top: 10px;
            width: 480px;
            height: 310px;
          }

          .item-detail {
            width: 420px;
            height: 290px;
          }
        }
      }
    }

    @media screen and (max-width: 900px) {
      .main-content {
        width: 100%;

        .content-item {
          .item-image {
            display: block;
            width: 100%;
            height: auto;
            border-radius: 0;
          }

          .item-detail {
            position: static;
            width: 100%;
            height: auto;
            padding: 40px 20px;
            border: none;
            border-bottom: 1px solid #ebebeb;
          }
        }
      }
    }
  }
}
</style>
