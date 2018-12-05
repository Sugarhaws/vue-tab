
<script>
  export default {
    name: 'Tab',
    data () {
      return {
        
      }
    },
    props: {
      title: {
        type: String,
        default: 'tab'
      },
      index: {
        type: [String,Number],
        required: true
      }
    },
    mounted() {
      // 将当前组件添加到tabs组件的panes变量中
      this.$parent.panes.push(this)
    },
    methods: {
      clickHandle () {
        //将点击当前元素的index值传递到tabs组件中
        this.$parent.sendIndex(this.index);
      }
      
    },
    computed: {
      //判断active类名存在的条件
      active () {
        return this.$parent.value == this.index;
      }
    },
    render () {
      //读取tab标签中的label属性
      let tab = this.title || this.$slots.title;
      //根据active类名是否存在来设计高亮效果
      let classNames = {
        tab: true,
        active: this.active
      }
      return (
        <li class={ classNames } onClick={this.clickHandle.bind(this)}>
          { tab }
        </li>
      )
    }
  }
</script>

<style scoped>

.tab{
  list-style:none;
  line-height:40px;
  margin-right:30px;
  position:relative;
  bottom:-2px;
  cursor:pointer;
}

.tab.active{
  border-bottom:2px solid blue;
  color: brown;
}

.tab.last-child{
  margin-right:0;
}


</style>