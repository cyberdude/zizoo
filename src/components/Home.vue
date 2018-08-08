<template>
  <div>

    <div class="container">
      <div id="sail_list">
        <div class="row sail-item">
          <div class="nabisco">Zizoo recommended</div>
          <div class="col-12 col-md-5 thumbnail">
          </div>

          <div class="col-12 col-md-7 description">

            <div class="row header-area">

              <div class="col-8 name-area">
                <div class="row">
                  <div class="col-10">
                    <h5>Jeannau Sun Odyssey 45.2 <span>2001</span></h5>
                    <div class="location">Split, Croatia</div>
                  </div>
                  <div class="col-2">
                    <img src="/static/heart.svg" class="heart">
                  </div>
                </div>
              </div>

              <div class="col-4 stats">
                <div class="row">
                  <div>
                    <div class="s-views"><span>HOT</span> 69 views</div>
                    <div class="relative-time">in the last 24 hours</div>
                  </div>
                </div>
              </div>

            </div> <!-- End Header area -->

            <div class="row capacity-reviews">

              <div class="col-2 stat-box">
                <div>
                  <span class="stat-value">
                    12.04m
                  </span>

                  <span class="stat-unit">
                    Length
                  </span>
                </div>
              </div>

              <div class="col-2 stat-box">
                <div>
                  <span class="stat-value">
                    4
                  </span>

                  <span class="stat-unit">
                    Cabins
                  </span>
                </div>
              </div>

              <div class="col-2 stat-box">
                <div>
                  <span class="stat-value">
                    10
                  </span>

                  <span class="stat-unit">
                    Guests
                  </span>
                </div>
              </div>

              <div class="col-6 stat-box">
                <div>
                  <span>
                    <div class="stars">
                      <svg height="24" width="20" class="star rating" data-rating="1" v-for="x in 5" :key="x">
                        <polygon points="9.9, 1.1, 3.3, 21.78, 19.8, 8.58, 0, 8.58, 16.5, 21.78" style="fill-rule:nonzero;"/>
                      </svg>
                    </div>
                  </span>
                  <span class="stat-unit">
                    3 Reviews
                  </span>
                </div>
              </div>

            </div>

            <div class="row closing-details">

              <div class="col-12 col-md-6 flex-details">

                <div class="row">
                  <div class="col-4 col-md-12">
                    <ul class="extra-notes">
                      <li>Sicherungsshein</li>
                      <li>Luxury</li>
                    </ul>
                  </div>

                    <div class="col-4 col-md-12 features">
                      <div class="info-unit">
                        SAIL TYPE
                      </div>

                      <div class="info-data">
                        Rolling Mainsail
                      </div>
                    </div>

                    <div class="col-4 col-md-12 features">
                      <div class="info-unit">
                        FREE EXTRAS
                      </div>

                      <div class="info-data">
                        AirCon, WiFi, Very Long Extra Description
                      </div>
                    </div>

                  </div>
              </div>

              <div class="col-12 col-md-6 cta-info">
                <div class="row no-gutters">
                <div class="col-6 col-md-12 cta-block price-area">
                  <div>
                  FROM <span class="price">€1,083.00</span>
                  <span class="recurrency">weekly</span>
                  <img src="/static/help-material.png"
                    srcset="/static/help-material@2x.png 2x,
                            /static/help-material@3x.png 3x"
                    class="help-bubble">
                    </div>
                </div>

                <div class="col-6 col-md-12 cta-block">
                  <div>

                    <div class="direct-info">
                    <img src="/static/flash-on-material.png"
                      srcset="/static/flash-on-material@2x.png 2x,
                              /static/flash-on-material@3x.png 3x"
                      class="flash">

                    Direct Booking
                    </div>

                    <a class="main-cta">
                      View Details
                    </a>
                  </div>
                </div>
              </div>
              </div>
            </div>
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

<style lang="scss" scoped>
@import '../scss/variables';
@import '../scss/mixins';

@import '~bootstrap/scss/functions';
@import '~bootstrap/scss/variables';
@import '~bootstrap/scss/mixins';

.heart {
  width: 16px;
  height: 13px;

  &:hover {
    opacity: .5;
    cursor: pointer;
  }
}

.nabisco {
  width: 146px;
  height: 22px;
  position: absolute;
  top: 21px;
  z-index: 10;
  background: $charcoalGrey;
  line-height: 0;
  color: #fff;
  font-size: 11px;
  text-transform: uppercase;
  font-weight: bold;
  display: flex;
  align-items: center;
  justify-content: center;
}

#sail_list {
  padding: 5px;
}

.sail-item {
  max-width: 875px;
  border: 1px solid $pinkishGrey;
  position: relative;
  margin: 10px auto;

  .thumbnail {
    position: relative;
    overflow: hidden;
    border: 10px solid #fff;
    min-height: 206px;
    &:before {
      @include absoluteMe();
      content: ' ';
      background: url(/static/boat-image-bg.jpg) no-repeat center;
      background-size: cover;
    }
  }

  .header-area {
    background: $white;
    height: 62px;
    > div {
      border: 1px solid $pinkishGrey;

      .row {
        align-items: center;
        justify-content: flex-start;
        text-align: left;
        display: flex;
        height: 100%;
      }
    }

    .name-area {
      border-right: 0;
      color: $charcoalGrey;
      .row {
        h5 {
          font-size: 16px;
          font-weight: bold;
          margin-bottom: 0;
          line-height: 20px;
          span {
            font-weight: normal;
            display: inline-block;
          }
        }

        .location {
          font-size: 12px;
        }
      }
    }

    .stats {
      color: $paleRed;
      font-size: 11px;
      line-height: 14px;
      > div {
        justify-content: center;

      }
      .s-views {
        font-weight: bold;

        span {
          width: 28px;
          height: 13px;
          border-radius: 1px;
          background: $paleRed;
          font-size: 9px;
          font-style: normal;
          letter-spacing: normal;
          color: #ffffff;
          align-items: center;
          display: inline-flex;
          justify-content: center;
        }
      }
    }
  }

  .capacity-reviews {
    .stat-box {
      border: 1px solid $pinkishGrey;
      border-top: 0;
      color: $charcoalGrey;
      height: 52px;
      align-items: center;
      justify-content: center;
      display: flex;

      > div {
        > span {
          display: block;
        }
      }

      .stat-value {
        color: $charcoalGrey;
        font-size: 14px;
        font-weight: 600;
      }
      .stat-unit {
        font-size: 10px;
        font-weight: normal;
        text-transform: uppercase;
      }

      .stars {
        transform: scale(.8);
        svg {
          fill: #f8e71c;
          &:hover {
            cursor: pointer;
            opacity: .5;
          }
        }
      }

      &:not(:first-child) {
        border-left: 0;
      }
    }
  }

  .closing-details {
    > div {
      border: 1px solid $pinkishGrey;
      border-top: 0;
      border-bottom: 0;
      &:not(:first-child) {
        border-left: 0;
      }
    }

    .flex-details {
      .row {
        align-items: center;
      }
      ul.extra-notes {
        list-style: none;
        padding: 0;
        margin-bottom: 0;
        width: 100%;
        height: 33px;
        align-items: center;
        display: flex;
        li {
          float: left;
          margin-right: 16px;
          padding-left: 14px;
          position: relative;
          font-size: 11px;
          color: rgba(54, 62, 64, 0.8);
          font-weight: 600;
          &:before {
            @include absoluteMe();

            width: 100%;
            content: '';
            background: url(/static/check-material.png) no-repeat 0 center;
            background-size: 12px;
          }
        }
      }

      .features {
        color: $charcoalGrey;
        text-align: left;
        margin-bottom: 8px;
        .info-unit {
          font-size: 10px;
        }
        .info-data {
          font-size: 12px;
          font-weight: 600;
        }
      }
    }

    .cta-info {
      padding: 0;

      .row.no-gutters {
        height: 100%;
        > div {
          display: flex;
          align-items: center;
          justify-content: center;
          height: 50%;
        }

      .cta-block {
        align-self: center;
        &:first-child {
          border-bottom: 1px solid $pinkishGrey;
        }
        .direct-info {
          font-size: 10px;
          line-height: 1.4;
          font-weight: bold;
          margin-bottom: 6px;
        }
        .main-cta {
          display: flex;
          align-items: center;
          justify-content: center;
          font-size: 16px;
          font-weight: bold;
          color: #fff;
          background: url(/static/cta-arrow.svg) no-repeat center;
          width: 191px;
          background-size: 100%;
          height: 32px;

          &:hover {
            cursor: pointer;
            opacity: .8;
          }
        }
      }
      .cta-block.price-area {
        height: 49px;
        color: $charcoalGrey;
        font-size: 10px;
        height: 40%;
        .price {
          font-size: 16px;
          font-weight: bold;
          margin: 0 2px 0 5px;
        }
        .recurrency {
          font-size: 11px;
          font-weight: 600;
        }
        .help-bubble {
          margin-left: 8px;
          position: relative;
          top: -2px;
        }
      }
      }
    }

    @include media-breakpoint-down(sm) {

      .flex-details {
        min-height: 75px;
        .row {
          height: 100%;
          ul.extra-notes {
            display: block;
            li {
              width: 100%;
              text-align: left;
              margin-bottom: 10px;
            }
          }
        }
      }

      .col-12.cta-info {
        border-top: 1px solid $pinkishGrey;
        height: 75px;
        .row.no-gutters {
          .cta-block {
            height: 100%;
            &:first-child {
              border-right: 1px solid $pinkishGrey;
              border-left: 1px solid $pinkishGrey;
            }

            &:last-child {
              border-bottom: 1px solid $pinkishGrey;
            }

            .main-cta {
              width: 147px;
            }
          }
        }
      }
    }

  }
}
</style>
