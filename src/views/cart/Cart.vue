<template>
  <div class="cart">
    <!-- 导航 -->
    <nav-bar class="nav-bar">
      <div slot="center">
        购物车({{catListLength}})
      </div>
    </nav-bar>

    <!-- 商品列表 -->
    <cart-list></cart-list>

    <!-- 底部汇总 -->
    <cart-bottom-bar></cart-bottom-bar>
  </div>
</template>
<script>
import navBar from "components/common/navbar/NavBar";
import { mapGetters } from "vuex";
import CartList from "./childComps/CartList";
import CartBottomBar from './childComps/CartBottomBar';
export default {
  name: "Cart",
  components: {
    navBar,
    CartList,
    CartBottomBar,
  },
  computed: {
    ...mapGetters(["catListLength"]),
  }
};
</script>
<style scoped>
.nav-bar {
  background: var(--color-tint);
  color: #fff;
}
</style>
