@use './base/reset';
@use './utilities/variables';

.container {
  background: url(../images/bg-mobile.svg) no-repeat top/100%, variables.$violet;
  min-height: 100vh;

  display: flex;

  & .wrap {
    max-width: 89.25rem;
    padding: 0 clamp(2rem, 5vw, 4.25rem);

    & .landing-page {
      margin: clamp(2rem, 5vw, calc(3.5rem - 2px)) 0 2rem;

      &__header {
        margin-left: 2px;
        width: clamp(129px, 16vw, 215px);
      }

      &__overview {
        margin-top: clamp(calc(3.75rem - 3px), 8vw, calc(5.25rem - 1px));

        display: flex;
        justify-content: center;
        flex-flow: row wrap;
        gap: calc(3.75rem - 3px);

        & .illustration {
          padding: 3px 5px;
        }

        & .summary {
          max-width: calc(32.75rem + 1px);
          color: variables.$white;
          text-align: center;

          & h1 {
            margin: 0;
            font-size: clamp(1.5rem, 5vw, 2.5rem);
            line-height: clamp(2.25rem, 6vw, 3.75rem);
            letter-spacing: -0.006em;

            & span {
              letter-spacing: -0.004em;
            }
          }

          & p {
            margin: clamp(13px, 3vw, 19px) 0 25px;
            padding: 0 .25rem;

            font-family: 'Open Sans', sans-serif;
            font-weight: 400;
            font-size: clamp(1rem, 2vw, calc(1rem + 2px));
            line-height: clamp(1.5rem, 6vw, calc(1.5rem + 3px));

            @media (min-width: 48rem) {
              padding: 0 .25rem 0 0;
            }
          }

          & button {
            background: variables.$white;
            color: variables.$violet;
            width: 12.5rem;
            padding: calc(0.75rem + 1px) 0 clamp(9px, 2vw, 1rem) 0;

            font-family: 'Poppins', sans-serif;
            font-weight: 400;
            font-size: clamp(0.75rem, 3vw, 18px);
            letter-spacing: -0.005em;

            border: none;
            border-radius: 100vw;
            box-shadow: 2px 4px 9px 3px rgba(0, 0, 0, 0.25);

            cursor: pointer;
            transition: 0.3s;

            &:hover {
              background: variables.$soft-magenta;
              color: variables.$white;

              transition: 0.3s;
            }
          }

          @media (min-width: 89.25rem) {
            margin-top: calc(3rem - 2px);
            text-align: start;
          }
        }

        @media (min-width: 48rem) {
          gap: 3rem;
        }
      }

      &__footer {
        margin-top: 3.5rem;

        & .social-media {
          padding: 0.5rem 0;

          & ul {
            display: flex;
            justify-content: center;
            flex-flow: row nowrap;
            gap: clamp(calc(0.75rem - 2px), 2vw, 1rem);

            & .link-item {
              color: variables.$white;

              width: clamp(28px, 5vw, 2.5rem);
              aspect-ratio: 1;
              padding: 1px 0 0 1px;
              font-size: clamp(12px, 2vw, calc(1rem + 2px));

              border-radius: 100vw;
              border: 1px solid variables.$white;

              display: flex;
              align-items: center;
              justify-content: center;

              transition: 0.3s;

              &:hover {
                color: variables.$soft-magenta;
                border-color: variables.$soft-magenta;
                transition: 0.3s;
              }

              @media (min-width: 48rem) {
                padding: 0;
              }
            }

            & .twitter {
              font-size: clamp(13px, 2vw, calc(1rem + 2px));
            }

            & .instagram {
              font-size: clamp(14px, 2vw, 1.3rem);
            }

            @media (min-width: 89.25rem) {
              justify-content: end;
            }
          }
        }

        @media (min-width: 89.25rem) {
          margin-top: calc(0.75rem - 2px);
        }
      }
    }
  }

  @media (min-width: 89.25rem) {
    background: url(../images/bg-desktop.svg) no-repeat left/contain, variables.$violet;
    // background: url(../design/desktop-design.jpg) no-repeat top left/100%, variables.$violet;
  }

  @media (min-width: 91rem) {
    align-items: center;
    justify-content: center;
  }
}