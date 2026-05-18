<template>
  <q-page class="row items-center justify-evenly">
    <q-img src="src/assets/landing.png" :ratio="16 / 9">
      <div class="text-center flex flex-center column bg-transparent full-height full-width">
        <div class="text-h2 text-weight-bold q-mb-lg">Globalization</div>
        <div class="text-h5 text-weight-medium">
          <div>It’s how the world's economies, cultures, and populations have grown</div>
          <div>increasingly tangled with one another.</div>
        </div>
        <div class="q-mt-xl q-gutter-x-md">
          <q-btn label="Overview" no-caps rounded class="custom-button" />
          <q-btn label="View effects" no-caps rounded class="custom-button" />
        </div>
      </div>
    </q-img>

    <div class="row flex flex-center q-mt-xl">
      <div class="col-6">
        <q-img src="src/assets/landing-2.png" />
      </div>
      <div class="col-6 q-pa-xl">
        <div class="text-h3">Connecting</div>
        <div class="text-h3 text-weight-bold">the Civilization</div>
        <div class="text-h6 text-weight-medium q-mt-lg">
          Trade and technology are the main drivers, and the ripple effects touch everything from
          how local economies function, to how governments make decisions, to whether people's basic
          rights are actually protected.
        </div>
      </div>
    </div>

    <q-img src="src/assets/landing-3.png" :ratio="16 / 9" class="q-mt-xl">
      <div class="text-left justify-center column absolute-full bg-transparent q-ml-xl">
        <div class="row">
          <div class="col-7">
            <div class="text-h3 text-weight-bold q-mb-lg">Overview about Globalization</div>
            <div class="text-body1 q-mb-md">
              Global trade in goods and services reached $32 trillion in 2022, with the UN Trade and
              Development agency warning of tougher conditions ahead. That figure alone shows how
              deeply interconnected global economies have become.
            </div>
            <div class="text-body1 q-mb-md">
              Globalization isn't just about breaking into new markets anymore. It's about keeping
              up with political shifts, digital disruption, and consumers who expect more, faster.
            </div>
            <div class="text-body1 q-mb-md">
              The WTO revised its 2025 global trade forecast upward to 2.4% growth, driven largely
              by booming demand for AI-related goods like semiconductors, servers, and
              telecommunications equipment, which accounted for nearly half of all merchandise trade
              expansion in the first half of the year.
            </div>
          </div>
        </div>
      </div>
    </q-img>

    <div class="q-pa-xl row justify-center">
      <div class="col-12 col-lg-11">
        <div class="q-mb-xl">
          <div class="text-h3 text-weight-bolder text-grey-10 q-mb-sm">
            The Effects of Globalization
          </div>
          <div class="text-h6 text-weight-regular text-grey-8">
            Globalization has led to increases in standards of living around the world, but not all
            of its effects are positive for everyone.
          </div>
        </div>

        <div class="row q-col-gutter-lg q-mt-md">
          <div class="col-12 col-md-3">
            <div class="row no-wrap q-gutter-x-sm">
              <q-icon name="check_circle_outline" color="positive" size="md" />
              <div class="col">
                <div class="text-primary text-weight-bold text-h5">
                  Trade and job creation have raised living standards
                </div>
                <div class="text-body1 q-mt-md">
                  More trade and job creation have raised living standards for a real number of
                  people. Globalization rewired the global economy in ways that opened doors that
                  didn't exist before.
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-md-3">
            <div class="row no-wrap q-gutter-x-sm">
              <q-icon name="check_circle_outline" color="positive" size="md" />
              <div class="col">
                <div class="text-primary text-weight-bold text-h5">
                  Given individuals and communities economic ground to stand on
                </div>
                <div class="text-body1 q-mt-md">
                  It's also given individuals and communities economic ground to stand on, letting
                  them preserve their cultural identity. Traditional crafts and art forms, for
                  example, now reach buyers worldwide through online platforms.
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-md-3">
            <div class="row no-wrap q-gutter-x-sm">
              <q-icon name="highlight_off" color="negative" size="md" />
              <div class="col">
                <div class="text-primary text-weight-bold text-h5">
                  Cultural homogenization is quietly eroding what makes local communities distinct
                </div>
                <div class="text-body1 q-mt-md">
                  Critics argue that cultural homogenization is quietly eroding what makes local
                  communities distinct, and that ceding control over critical technologies leaves
                  nations vulnerable, both economically and in terms of security.
                </div>
              </div>
            </div>
          </div>

          <div class="col-12 col-md-3">
            <div class="row no-wrap q-gutter-x-sm">
              <q-icon name="highlight_off" color="negative" size="md" />
              <div class="col">
                <div class="text-primary text-weight-bold text-h5">A widening gap</div>
                <div class="text-body1 q-mt-md">
                  Research also points to a widening gap: globalization tends to benefit the highly
                  educated while putting downward pressure on wages for workers without specialized
                  skills.
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup lang="ts">

</script>

<style setup lang="scss">
</style>
