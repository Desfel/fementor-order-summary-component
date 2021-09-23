<template>
  <div class="page-wrapper">
    <div class="card-wrapper">
      <img class="card-hero" src="@/assets/img/illustration-hero.svg" alt="Hero"/>

      <div class="card-content">
        <p class="card-title">Order Summary</p>

        <p class="card-summary">
          You can now listen to millions of songs, audiobooks, and podcasts on
          any device anywhere you like!
        </p>

        <div class="card-plan-info">
          <img src="@/assets/img/icon-music.svg" alt="Music Icon" />

          <div class="card-plan-text">
            <p class="plan-type">Annual Plan</p>
            <p class="plan-price">$59.99/year</p>
          </div>

          <a href="#" class="action-btn">Change</a>
        </div>

        <button class="cta-btn" type="button">Proceed to Payment</button>
        <a href="#" class="cancel-btn">Cancel Order</a>
      </div>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 20px;

  .card-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: $light;
    box-shadow: 0 40px 40px -20px rgba(13, 48, 189, 0.151826);
    border-radius: 20px;
    text-align: center;
    max-width: 450px;

    img {
      max-width: 100%;
      border-radius: 15px 15px 0 0;
    }
  }

  .card-content {
    padding: 45px 48px 48px;


    @media (max-width: 767px) {
      padding: 32px 24px;
    }

    .card-title {
      font-weight: 900;
      font-size: 28px;
      line-height: 37px;
      color: $neutralColor3;
      margin-bottom: 18px;

      @media (max-width: 767px) {
        font-size: 22px;
        line-height: 29px;
      }
    }

    .card-summary {
      font-weight: 500;
      font-size: 16px;
      line-height: 26px;
      color: $neutralColor2;


      @media (max-width: 767px) {
        font-size: 15px;
        line-height: 25px;
      }
    }

    .cta-btn {
      width: 100%;
      padding: 15px 0;
      margin-bottom: 32px;
      background: $primaryColor2;
      font-weight: 900;
      font-size: 15px;
      line-height: 20px;
      color: $light;
      border: none;
      border-radius: 11px;
      cursor: pointer;
      box-shadow: 0 20px 20px rgba(56, 42, 225, 0.190291);
      transition: background .3s ease-in-out;

      &:hover {
        background: lighten($primaryColor2, 15%);
      }

      @media (max-width: 767px) {
        font-size: 15px;
        line-height: 20px;
      }
    }

    .cancel-btn {
      font-weight: 900;
      font-size: 15px;
      line-height: 20px;
      color: $neutralColor2;
      transition: color .3s ease-in-out;

      &:hover {
        color: darken($neutralColor2, 45%);
      }

      @media (max-width: 767px) {
        font-size: 15px;
        line-height: 20px;
      }
    }
  }

  .card-plan-info {
    display: flex;
    align-items: center;
    padding: 25px 24px;
    margin: 20px 0 32px;
    border-radius: 11px;
    background: $neutralColor1;

    @media (max-width: 767px) {
      padding: 16px;
    }

    .card-plan-text {
      margin-left: 20px;

      p {
        font-size: 16px;
        line-height: 21px;

        @media (max-width: 767px) {
          font-size: 14px;
          line-height: 19px;
        }
      }

      .plan-type {
        font-weight: 900;
        color: $neutralColor3;
      }

      .plan-price {
        margin-top: 5px;
        font-weight: 500;
        color: $neutralColor2;
      }
    }

    .action-btn {
      margin-left: auto;
      font-size: 14px;
      line-height: 19px;
      text-decoration: underline;
      font-weight: 700;
      color: $primaryColor2;
      transition: color .3s ease-in-out;

      @media (max-width: 767px) {
        font-size: 13px;
        line-height: 17px;
      }

      &:hover {
        text-decoration: none;
        color: lighten($primaryColor2, 15%);
      }
    }
  }
}
</style>
