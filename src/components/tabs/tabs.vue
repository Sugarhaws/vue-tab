
<script>
import TabContent from './tabContent'
  export default {
    name: 'Tabs',
    components: {
      TabContent
    },
    data () {
      return {
        panes: [],  //用于承载tab组件
        value: '1'  //用于判断tab组件是否需要添加active类名的关键因素之一
      }
    },

    methods: {
      sendIndex (index) {
        this.value = index;
      }
    },
    render () {
      return (
        <div  class="tabs">
          <ul class="tabs-header">
            { this.$slots.default }
          </ul>
          <TabContent panes={this.panes}/>
        </div>
        
      )
    }
  }
</script>

<style scoped>
.tabs-header{
  display:flex;
  list-style:none;
  margin:0;
  padding:0;
  border-bottom:2px solid #ededed;
}
</style>