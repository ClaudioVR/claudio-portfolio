<script>
import { Bubble } from "vue-chartjs";

export default {
  extends: Bubble,
  // eslint-disable-next-line vue/require-prop-types
  props: ["data", "options"],
  mounted() {
    this.renderChart(this.data, this.options);
  },
};
</script>