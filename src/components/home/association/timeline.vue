<template>
  <section id="timeline" class="content">
    <img src="@/assets/svg/logo.svg" :alt="$t('association.logo') + '.'" />
    <article>
      <font-awesome-icon icon="fa-solid fa-caret-up" />
      <section>
        <article>
          <header class="big">
            2022
            <i></i>
          </header>
          <section>
            <div>
              <h3>{{ $t("association.timeline.2022.2.title") }}</h3>
              <p>{{ $t("association.timeline.2022.2.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2022.1.title") }}</h3>
              <p>{{ $t("association.timeline.2022.1.description") }}</p>
            </div>
          </section>
        </article>
        <article>
          <header>
            2021
            <i></i>
          </header>
          <section>
            <div>
              <h3>{{ $t("association.timeline.2021.3.title") }}</h3>
              <p>{{ $t("association.timeline.2021.3.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2021.2.title") }}</h3>
              <p>{{ $t("association.timeline.2021.2.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2021.1.title") }}</h3>
              <p>{{ $t("association.timeline.2021.1.description") }}</p>
            </div>
          </section>
        </article>
        <article>
          <header>
            2020
            <i></i>
          </header>
          <section>
            <div>
              <h3>{{ $t("association.timeline.2020.2.title") }}</h3>
              <p>{{ $t("association.timeline.2020.2.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2020.1.title") }}</h3>
              <p>{{ $t("association.timeline.2020.1.description") }}</p>
            </div>
          </section>
        </article>
        <article>
          <header>
            2019
            <i></i>
          </header>
          <section>
            <div>
              <h3>{{ $t("association.timeline.2019.3.title") }}</h3>
              <p>{{ $t("association.timeline.2019.3.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2019.2.title") }}</h3>
              <p>{{ $t("association.timeline.2019.2.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2019.1.title") }}</h3>
              <p>{{ $t("association.timeline.2019.1.description") }}</p>
            </div>
          </section>
        </article>
        <article>
          <header>
            2018
            <i></i>
          </header>
          <section>
            <div>
              <h3>{{ $t("association.timeline.2018.2.title") }}</h3>
              <p>{{ $t("association.timeline.2018.2.description") }}</p>
            </div>
            <div>
              <h3>{{ $t("association.timeline.2018.1.title") }}</h3>
              <p>{{ $t("association.timeline.2018.1.description") }}</p>
            </div>
          </section>
        </article>
        <article>
          <header>
            2017
            <i></i>
          </header>
          <section>
            <h3>{{ $t("association.timeline.2017.1.title") }}</h3>
            <p>{{ $t("association.timeline.2017.1.description") }}</p>
          </section>
        </article>
        <article>
          <header class="big">
            2015
            <i></i>
          </header>
          <section>
            <h3>{{ $t("association.timeline.2015.1.title") }}</h3>
            <p>{{ $t("association.timeline.2015.1.description") }}</p>
          </section>
        </article>
      </section>
    </article>
  </section>
</template>

<script>
export default {
  name: "timelineAssociationComponent",
};
</script>

<style scoped lang="scss">
#timeline {
  position: relative;
  overflow: hidden;

  & > img {
    width: 34%;
    min-width: 400px;
    z-index: 1;
    position: absolute;
    left: 3vw;
    bottom: -150px;
    opacity: 0.04;
    transform: rotate(-20deg);

    @media only screen and (min-width: 1200px) {
      & {
        bottom: -150px;
      }
    }
  }

  article {
    &:before {
      content: "";
      position: absolute;
      top: 40px;
      left: calc(50% - 1px);
      bottom: 0;
      width: 6px;
      background-color: #fff;
    }

    & > svg {
      font-size: 2.4em;
      position: absolute;
      top: 18px;
      left: calc(50% - 10px);
      transform: scaleY(1.4);
    }

    section article {
      width: calc(50% - 50px);
      float: left;
      padding: 26px 0;
      clear: both;
      text-align: right;

      &:not(:first-child) {
        margin-top: -100px;
      }

      &:last-child {
        margin-top: -10px;
      }

      header {
        font-size: 32px;
        margin-bottom: 12px;
        position: relative;
        display: flex;
        flex-flow: row-reverse nowrap;
        align-items: center;
        font-family: var(--title-font);
        font-weight: bold;
        color: var(--green-touch);
        gap: 14px;

        i {
          flex-grow: 1;
          border-top: 4px dotted #656565;

          &:before {
            z-index: 1;
            content: "";
            position: absolute;
            border-radius: 50%;
            background-color: var(--green-touch);
            width: 8px;
            height: 8px;
            right: -56px;
            top: calc(50% - 4px);
          }
        }

        &:before {
          content: "";
          position: absolute;
          width: 12px;
          height: 12px;
          border: 4px solid #ffffff;
          background-color: var(--bg-color);
          border-radius: 100%;
          top: 50%;
          transform: translateY(-50%);
          right: -62px;
          z-index: 1;
        }

        &.big {
          &:before {
            width: 24px;
            height: 24px;
            transform: translate(6px, -50%);
          }

          i:before {
            width: 20px;
            height: 20px;
            top: calc(50% - 10px);
            right: -62px;
          }
        }
      }

      section {
        div:not(:first-of-type) {
          margin-top: 30px;
        }

        h3 {
          text-transform: uppercase;
          margin-bottom: 10px;
          font-size: 1.5em;
          font-family: var(--title-font);
        }

        p {
          line-height: 1.4em;
          color: var(--subtext-color);
        }
      }

      &:nth-child(2n) {
        text-align: left;
        float: right;

        header {
          flex-flow: row nowrap;

          i:before {
            right: 0;
            left: -52px;
            top: calc(50% - 4px);
          }

          &:before {
            left: -58px;
          }

          &.big {
            &:before {
              transform: translate(-6px, -50%);
            }

            i:before {
              width: 20px;
              height: 20px;
              top: calc(50% - 10px);
              left: -58px;
            }
          }
        }
      }
    }
  }
}

@media only screen and (max-width: 650px) {
  #timeline {
    & > img {
      min-width: 300px;
      bottom: -120px;
    }

    article {
      &:before {
        left: 27px;
      }

      & > svg {
        left: 18px;
      }

      section article {
        width: calc(100% - 46px) !important;
        float: right !important;
        text-align: left !important;

        &:not(:first-child) {
          margin-top: -20px !important;
        }

        header {
          flex-flow: row nowrap !important;

          i:before {
            left: -38px !important;
          }

          &:before {
            left: -44px !important;
          }

          &.big {
            &:before {
              transform: translate(-6px, -50%);
            }

            i:before {
              left: -44px !important;
            }
          }
        }
      }
    }
  }
}
</style>
