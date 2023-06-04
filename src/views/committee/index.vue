<template>
  <div class="container" style="min-height: 40rem;padding: 2rem 0">
    <h1>COMMITTEE</h1>
    <hr class="hr">
    <div class="row row-cols-1 row-cols-md-4 g-4">
      <div class="col" v-for="m in members" v-bind:key="m.name">
        <div class="card" style="height: 500px">
          <img :src="m.img" class="card-img-top" :alt="m.name" style="height: 350px">
          <div class="card-body">
            <h5 class="card-title">{{m.name}}</h5>
            <div style="height: 60px">
              <p style="margin: 0;font-size: 1rem" class="card-text">{{m.institute}}</p>
              <p style="margin: 0;font-size: 1rem" class="card-text">{{m.email}}</p>
            </div>

            <p v-show="m.link" style="margin: 0;text-align: right"><a :href="m.link"  class="link-primary link-offset-2 link-underline-opacity-25 link-underline-opacity-100-hover">Link</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommitteeMembers',
  data() {
    return {
      members: [
        { name: 'Daniel Falush', institute: 'Institute Pasteur Shanghai, CAS', email: 'daniel.falush@ips.ac.cn', link: "http://sourcedb.shanghaipasteur.cas.cn/zw/kydw/yjzz/201911/t20191119_5438491.html", img: require('@/assets/img/committee/1.png') },
        { name: 'Jialu Chen', institute: 'Institute Pasteur Shanghai, CAS', email: 'jlchen@ips.ac.cn', link: '', img: require('@/assets/img/committee/2.png') },
        { name: 'Shuhua Xu', institute: 'Fudan University', email: 'xushua@fudan.edu.cn', link: 'https://homo.fudan.edu.cn/b6/18/c18452a177688/page.htm', img: require('@/assets/img/committee/3.png') },
        { name: 'Kai Ye', institute: 'Xi’an Jiaotong University', email: 'kaiye@xjtu.edu.cn', link: 'http://www.xjtu.edu.cn/jsnr.jsp?urltype=tree.TreeTempUrl&wbtreeid=1632&wbwbxjtuteacherid=1992', img: require('@/assets/img/committee/4.png') },
        { name: 'Jian Lu', institute: 'School of Life Sciences, Peking University', email: 'LUJ@pku.edu.cn', link: 'https://bio.pku.edu.cn/homes/Index/news_cont_jl/17/46.html', img: require('@/assets/img/committee/5.png') },
        { name: 'Hua Chen', institute: 'Beijing Institute of Genomics, CAS', email: 'chenh@big.ac.cn', link: 'http://www.big.ac.cn/sourcedb_big_cas/zw/zjrc/yjy/201506/t20150630_4381456.html', img: require('@/assets/img/committee/6.png') },
        { name: 'Chaolong Wang', institute: 'Huazhong University of Science and Technology', email: 'chaolong@hust.edu.cn', link: 'http://gwxy.tjmu.edu.cn/info/1016/1373.htm', img: require('@/assets/img/committee/7.png') },
        { name: 'Xuemei Lu', institute: 'Kunming Institute of Zoology, CAS', email: 'xuemeilu@mail.kiz.ac.cn', link: 'https://people.ucas.edu.cn/~3979404', img: require('@/assets/img/committee/8.png') },
      ]
    }
  }
}
</script>

<style scoped>

</style>
