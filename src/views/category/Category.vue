<template>
  <div class="wrapper" >
    <back-top @click.native="backClick" v-show="isShow"></back-top>
    <ul class="content">
      <li>滚动1</li>
      <li>滚动2</li>
      <li>滚动3</li>
      <li>滚动4</li>
      <li>滚动5</li>
      <li>滚动6</li>
      <li>滚动7</li>
      <li>滚动8</li>
      <li>滚动9</li>
      <li>滚动10</li>
      <li>滚动11</li>
      <li>滚动12</li>
      <li>滚动13</li>
      <li>滚动14</li>
      <li>滚动15</li>
      <li>滚动16</li>
      <li>滚动17</li>
      <li>滚动18</li>
      <li>滚动19</li>
      <li>滚动20</li>
      <li>滚动21</li>
      <li>滚动22</li>
      <li>滚动23</li>
      <li>滚动24</li>
      <li>滚动25</li>
      <li>滚动26</li>
      <li>滚动27</li>
      <li>滚动28</li>
      <li>滚动29</li>
      <li>滚动30</li>
      <li>滚动31</li>
      <li>滚动32</li>
      <li>滚动33</li>
      <li>滚动34</li>
      <li>滚动35</li>
      <li>滚动36</li>
      <li>滚动37</li>
      <li>滚动38</li>
      <li>滚动39</li>
      <li>滚动40</li>
      <li>滚动41</li>
      <li>滚动42</li>
      <li>滚动43</li>
      <li>滚动44</li>
      <li>滚动45</li>
      <li>滚动46</li>
      <li>滚动47</li>
      <li>滚动48</li>
      <li>滚动49</li>
      <li>滚动50</li>
      <li>滚动51</li>
      <li>滚动52</li>
      <li>滚动53</li>
      <li>滚动54</li>
      <li>滚动55</li>
      <li>滚动56</li>
      <li>滚动57</li>
      <li>滚动58</li>
      <li>滚动59</li>
      <li>滚动60</li>
      <li>滚动61</li>
      <li>滚动62</li>
      <li>滚动63</li>
      <li>滚动64</li>
      <li>滚动65</li>
      <li>滚动66</li>
      <li>滚动67</li>
      <li>滚动68</li>
      <li>滚动69</li>
      <li>滚动70</li>
      <li>滚动71</li>
      <li>滚动72</li>
      <li>滚动73</li>
      <li>滚动74</li>
      <li>滚动75</li>
      <li>滚动76</li>
      <li>滚动77</li>
      <li>滚动78</li>
      <li>滚动79</li>
      <li>滚动80</li>
      <li>滚动81</li>
      <li>滚动82</li>
      <li>滚动83</li>
      <li>滚动84</li>
      <li>滚动85</li>
      <li>滚动86</li>
      <li>滚动87</li>
      <li>滚动88</li>
      <li>滚动89</li>
      <li>滚动90</li>
      <li>滚动91</li>
      <li>滚动92</li>
      <li>滚动93</li>
      <li>滚动94</li>
      <li>滚动95</li>
      <li>滚动96</li>
      <li>滚动97</li>
      <li>滚动98</li>
      <li>滚动99</li>
      <li>滚动100</li>
    </ul>
  </div>
</template>
<script>
import BScroll from 'better-scroll'
import BackTop from '../../components/content/backTop/BackTop.vue'
import {backTopMixin} from 'common/mixin'

export default {
  components: { BackTop },
  name:"Category",
  data(){
    return{
      scroll:null
    }
  },
  mixins:[backTopMixin],
  mounted(){
    this.scroll = new BScroll(".wrapper",{
      probeType:3,
      pullUpLoad:true
    })
    // 获取当前滚动位置
    this.scroll.on("scroll",(position)=>{
      // console.log(position);
    })
    // 滚动到底部时 触发函数
    this.scroll.on("pullingUp",()=>{
      // console.log("上拉加载更多");
      this.scroll.finishPullUp()
    })
  },
  methods:{

  }
}
</script>
<style scoped>
.wrapper{
  background:red;
  height: 100%;
  overflow: hidden;
}
</style>
