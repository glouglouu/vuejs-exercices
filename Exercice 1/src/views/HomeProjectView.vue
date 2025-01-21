<script lang="ts" setup>
import HomeCard from '@/components/HomeCard.vue';
import cards from '../cards.json'
</script>
<template>
<div class="container project-box">
        <section class="dashboard">
          <div class="project">
            <h4>Your Projects</h4>
            <div class="project-grid">
              <HomeCard v-for="card in cards" :key="card.id" :card="card"/>
              </div>
            </div>
          <section class="side">
            <div class="announcement">
              <h4>Announcements</h4>
              <div class="background-box">
                <div class="anounce">
                  <h5>Site Maintenance</h5>
                  <p>
                    Lorem ipsum dolor sit amet, officia excepteur ex fugiat
                    reprehenderit enim labore culpa sint ad nisi Lorem pariatur
                    mollit ex esse exercitation amet. Nisi anim cupidatat
                    excepteur officia. Reprehenderit nostrud nostrud ipsum Lorem
                    est aliquip amet voluptate voluptate dolor minim nulla est
                    proident. Nostrud officia pariatur ut officia. Sit irure
                    elit esse ea nulla sunt ex occaecat reprehenderit commodo
                    officia dolor Lorem duis laboris cupidatat officia
                    voluptate. Culpa proident adipisicing id nulla nisi laboris
                    ex in Lorem sunt duis officia eiusmod. Aliqua reprehenderit
                    commodo ex non excepteur duis sunt velit enim. Voluptate
                    laboris sint cupidatat ullamco ut ea consectetur et est
                    culpa et culpa duis.
                  </p>
                </div>
                <hr />
                <div class="anounce">
                  <h5>Community Share Day</h5>
                  <p>
                    Lorem ipsum dolor sit amet, officia excepteur ex fugiat
                    reprehenderit enim labore culpa sint ad nisi Lorem pariatur
                    mollit ex esse exercitation amet. Nisi anim cupidatat
                    excepteur officia. Reprehenderit nostrud nostrud ipsum Lorem
                    est aliquip amet voluptate voluptate dolor minim nulla est
                    proident. Nostrud officia pariatur ut officia. Sit irure
                    elit esse ea nulla sunt ex occaecat reprehenderit commodo
                    officia dolor Lorem duis laboris cupidatat officia
                    voluptate. Culpa proident adipisicing id nulla nisi laboris
                    ex in Lorem sunt duis officia eiusmod. Aliqua reprehenderit
                    commodo ex non excepteur duis sunt velit enim. Voluptate
                    laboris sint cupidatat ullamco ut ea consectetur et est
                    culpa et culpa duis.
                  </p>
                </div>
                <hr />
                <div class="anounce">
                  <h5>Updated Privacy Policy</h5>
                  <p>
                    Lorem ipsum dolor sit amet, officia excepteur ex fugiat
                    reprehenderit enim labore culpa sint ad nisi Lorem pariatur
                    mollit ex esse exercitation amet. Nisi anim cupidatat
                    excepteur officia. Reprehenderit nostrud nostrud ipsum Lorem
                    est aliquip amet voluptate voluptate dolor minim nulla est
                    proident. Nostrud officia pariatur ut officia. Sit irure
                    elit esse ea nulla sunt ex occaecat reprehenderit commodo
                    officia dolor Lorem duis laboris cupidatat officia
                    voluptate. Culpa proident adipisicing id nulla nisi laboris
                    ex in Lorem sunt duis officia eiusmod. Aliqua reprehenderit
                    commodo ex non excepteur duis sunt velit enim. Voluptate
                    laboris sint cupidatat ullamco ut ea consectetur et est
                    culpa et culpa duis.
                  </p>
                </div>
              </div>
            </div>
            <div>
              <h4>Trending</h4>
              <div class="background-box trending">
                <div class="trend">
                  <figure>
                    <img
                      class="avatar"
                      src="https://robohash.org/irwi32.png?set=set4"
                      alt="avatar"
                    />
                  </figure>
                  <div class="trend-details">
                    <h6>@tegan</h6>
                    <p>World Peace Builder</p>
                  </div>
                </div>
                <div class="trend">
                  <figure>
                    <img
                      class="avatar"
                      src="https://robohash.org/ijrwi32.png?set=set4"
                      alt="avatar"
                    />
                  </figure>
                  <div class="trend-details">
                    <h6>@morgan</h6>
                    <p>Super cool Project</p>
                  </div>
                </div>
                <div class="trend">
                  <figure>
                    <img
                      class="avatar"
                      src="https://robohash.org/irw2.png?set=set4"
                      alt="avatar"
                    />
                  </figure>
                  <div class="trend-details">
                    <h6>@kindall</h6>
                    <p>Life Changing App</p>
                  </div>
                </div>
                <div class="trend">
                  <figure>
                    <img
                      class="avatar"
                      src="https://robohash.org/ireqwe2.png?set=set4"
                      alt="avatar"
                    />
                  </figure>
                  <div class="trend-details">
                    <h6>@alex</h6>
                    <p>No Traffic Maker</p>
                  </div>
                </div>
              </div>
            </div>
          </section>
        </section>
      </div>
</template>
<style></style>
