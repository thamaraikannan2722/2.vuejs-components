<template>
  <Components name="Bruce" heroName="Batman" />
  <Components name="Clark" heroName="Superman" />
  <Components name="Diana" heroName="Wonder Woman" />
  <Components :name="name" :heroName="channel" />

  <PropsValidations
    id="my-article"
    title="Article Title"
    :likes="45"
    :isPublished="true"
  />

  <ComponentC />
  <h3>App Component username - {{ name }}</h3>

  <button @click="showPopup = true">Show Popup</button>
  <ComponentEvents v-show="showPopup" @close="closePopup" />
  <Input v-model="name" />

  <Slots></Slots>
  <Slots>Card Content</Slots>
  <Slots>
    <h2>Card Content</h2>
  </Slots>
  <Slots class="slot">
    <img
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1200px-HTML5_logo_and_wordmark.svg.png"
    />
  </Slots>

  <Slots class="slot">
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1200px-HTML5_logo_and_wordmark.svg.png"
      />
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </Slots>

  <SlotProps>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} {{ slotProps.lastName }}
    </template>
  </SlotProps>

  <SlotProps>
    <template v-slot:default="slotProps">
      {{ slotProps.lastName }} {{ slotProps.firstName }}
    </template>
  </SlotProps>

  <SlotProps>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }}
    </template>
  </SlotProps>

  <h4>App component text</h4>
  <ComponentStyles />

  <button @click="activeTab = 'TabA'">Tab A</button>
  <button @click="activeTab = 'TabB'">Tab B</button>
  <button @click="activeTab = 'TabC'">Tab C</button>

  <keep-alive>
    <component :is="activeTab" />
  </keep-alive>

  <!-- <TabA v-if="activeTab === 'TabA'"/>
  <TabB v-if="activeTab === 'TabB'"/>
  <TabC v-if="activeTab === 'TabC'"/> -->
  <teleport to="#portal-root">
    <TeleportComponent />
  </teleport>
</template>

<script>
import Components from "../src/components/14.Components";
import PropsValidations from "../src/components/15.Prop-Types_and_Validations";
import ComponentC from "../16.Provide_and_Inject/ComponentC";
import ComponentEvents from "../src/components/17.Component_Events";
import Input from "../src/components/18.Components_and_v-model";
import Slots from "../src/components/19.Slots";
import SlotProps from "../src/components/20.Slot_Props";
import ComponentStyles from "../src/components/21.Component_Styles";
import TabA from "../22.Dynamic_Components/Tab A";
import TabB from "../22.Dynamic_Components/Tab B";
import TabC from "../22.Dynamic_Components/Tab C";
import TeleportComponent from "../src/components/22.Teleport_Component";

export default {
  name: "App",
  components: {
    Components,
    PropsValidations,
    ComponentC,
    ComponentEvents,
    Input,
    Slots,
    SlotProps,
    ComponentStyles,
    TabA,
    TabB,
    TabC,
    TeleportComponent,
  },
  data() {
    return {
      name: "Ashwin",
      channel: "AM Studios Official",
      username: "Ashwin",
      showPopup: false,
      activeTab: "TabA",
    };
  },
  methods: {
    closePopup(name) {
      (this.showPopup = false), console.log("name -", name);
    },
  },
  provide() {
    return {
      username: this.name,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.slot img {
  width: 100px;
  height: 100px;
}
h4 {
  color: orange;
}
</style>
