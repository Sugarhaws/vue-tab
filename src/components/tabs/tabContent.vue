
<script>
  export default {
    name: 'TabContent',
    props: {
      panes: {
        type: Array,
        defulat: function () {
          return [];
        }
      }
    },


    render () {
      let contents = this.panes.map((ele,index) => {
        //根据active类名是否存在来决定渲染的内容
        return ele.active ? ele.$slots.default : '';
      })

      return (
        <div>
          {contents}
        </div>
      )
    }
  }
</script>

<style scoped>

</style>