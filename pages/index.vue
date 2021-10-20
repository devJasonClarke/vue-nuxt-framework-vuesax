<template>
  <div>
    <vs-navbar v-model="active" center-collapsed>
      <vs-navbar-item id="guide" :active="active == 'guide'">
        Guide
      </vs-navbar-item>
      <vs-navbar-item id="docs" :active="active == 'docs'">
        Documents
      </vs-navbar-item>
      <vs-navbar-item id="components" :active="active == 'components'">
        Components
      </vs-navbar-item>
      <vs-navbar-item id="license" :active="active == 'license'">
        license
      </vs-navbar-item>
      <template #right>
        <vs-button flat>Login</vs-button>
        <vs-button>Get Started</vs-button>
      </template>
    </vs-navbar>
    <vs-button transparent :active="active == 0" @click="active = 0">
      Active
    </vs-button>
    <vs-button transparent :active="active == 1" @click="active = 1">
      Default
    </vs-button>
    <vs-button transparent disabled> Disabled </vs-button>
    <vs-button @click="openNotification"> Open Notification </vs-button>
    <vs-card>
      <template #title>
        <h3>Pot with a plant</h3>
      </template>
      <template #img>
        <img src="/foto5.png" alt="" />
      </template>
      <template #text>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
      </template>
      <template #interactions>
        <vs-button danger icon>
          <i class="bx bx-heart"></i>
        </vs-button>
        <vs-button class="btn-chat" shadow primary>
          <i class="bx bx-chat"></i>
          <span class="span"> 54 </span>
        </vs-button>
      </template>
    </vs-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    active: 'guide',
  }),
  methods: {
    openNotification() {
      this.$vs.notification({
        title: 'Documentation Vuesax 4.0+',
        text: `These documents refer to the latest version of vuesax (4.0+),
            to see the documents of the previous versions you can do it here 👉 Vuesax3.x`,
      })
    },
  },
}
</script>
