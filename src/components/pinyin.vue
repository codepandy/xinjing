<template>
  <div>
    <row v-for="item in scriptures" v-bind="item" :key="item.text" />
  </div>
</template>

<script setup lang="ts">
import row from "./row.vue";

// 经文 xíng shēn bō rě bō luó mì duō shí
const scriptures = [
  {
    text: "般若波罗蜜多心经",
    ruby: "bō rě bō luó mì duō xīn jīng",
    explain: "",
    isTitle: true,
  },
  {
    text: "观自在菩萨，行深般若波罗蜜多时",
    ruby: "guān zì zài pú sà , xíng shēn bō rě bō luó mì duō shí",
    explain: "【解释】观音菩萨，深入的修行心经时",
  },
  {
    text: "照见五蕴皆空，度一切苦厄。",
    ruby: "zhào jiàn wǔ yùn jiē kōng ， dù yī qiē kǔ è",
    explain:
      "【解释】看到五蕴：形相、情欲、意念、行为、心灵，都是空的，就将一切苦难置之度外",
  },
  {
    text: "舍利子，色不异空，空不异色",
    ruby: "shè lì zǐ ， sè bù yì kōng ， kōng bù yì sè",
    explain: "【解释】菩萨对学生舍利子说，形相不异乎空间，空间不异乎形相",
  },
  {
    text: "色即是空，空即是色。",
    ruby: "sè jí shì kōng ， kōng jí shì sè",
    explain: "【解释】所以形相等于空间，空间等于形相",
  },
  {
    text: "受想行识，亦复如是。",
    ruby: "shòu xiǎng xíng shí ， yì fù rú shì",
    explain: "【解释】情欲、意念、行为、心灵，都是一样的",
  },
  {
    text: "舍利子，是诸法空相",
    ruby: "shè lì zǐ ， shì zhū fǎ kōng xiāng",
    explain: "【解释】舍利子呀，一切法则都是空的",
  },
  {
    text: "不生不灭，不垢不净，不增不减",
    ruby: "bù shēng bù miè，bù gòu bù jìng，bù zēng bù jiǎn",
    explain: "【解释】不生不灭，不垢不净，不增不减",
  },
  {
    ruby: "shì gù kōng zhōng wú sè ， wú shòu xiǎng xíng shí",
    text: "是故空中无色，无受想行识",
    explain: "【解释】因此空间是没有形相的，也没有情欲、意念、行为和心灵",
  },
  {
    ruby: "wú yǎn ěr bí shé shēn yì, wú sè shēng xiāng wèi chù fǎ",
    text: "无眼耳鼻舌身意，无色声香味触法",
    explain:
      "【解释】没有眼、耳、鼻、舌、身、意等六根，更没有色、声、香、味、触、法等六尘",
  },
  {
    ruby: "wú yǎn jiè ， nǎi zhì wú yì shí jiè",
    text: "无眼界，乃至无意识界",
    explain: "【解释】没有眼睛所能看到的界限，直到没有心灵所能感受的界限",
  },
  {
    ruby: "wú wú míng ， yì wú wú míng jìn",
    text: "无无明，亦无无明尽",
    explain: "【解释】没有不能了解的，也没有不能了解的尽头",
  },
  {
    ruby: "nǎi zhì wú lǎo sǐ ， yì wú lǎo sǐ jìn",
    text: "乃至无老死，亦无老死尽。",
    explain: "【解释】直到没有老和死，也没有老和死的尽头",
  },
  {
    ruby: "wú kǔ jí miè dào ， wú zhì yì wú dé ， yǐ wú suǒ dé gù",
    text: "无苦集灭道，无智亦无得，以无所得故。",
    explain:
      "【解释】没有痛苦的集合以及修道的幻灭，不用智慧去强求，所以得到与否并不重要",
  },
  {
    ruby: "pú tí sà duǒ ， yī bō rě bō luó mì duō gù ， xīn wú guà ài",
    text: "菩提萨埵，依般若波罗蜜多故，心无挂碍。",
    explain: "【解释】菩萨觉悟之后，依照心经，心中没有碍",
  },
  {
    ruby: "wú guà ài gù ， wú yǒu kǒng bù",
    text: "无挂碍故，无有恐怖",
    explain: "【解释】由于没有碍，所以不恐怖",
  },
  {
    ruby: "yuǎn lí diān dǎo mèng xiǎng ， jiū jìng niè pán",
    text: "远离颠倒梦想，究竟涅槃。",
    explain: "【解释】远离颠倒梦想 ，最后达到彼岸",
  },
  {
    ruby: "sān shì zhū fó ， yī bō rě bō luó mì duō gù",
    text: "三世诸佛，依般若波罗蜜多故",
    explain: "【解释】过去、现在和未来的三世诸佛，依照心经",
  },
  {
    ruby: "dé ā nuò duō luó sān miǎo sān pú tí",
    text: "得阿耨多罗三藐三菩提。",
    explain: "【解释】得到无上、正宗、正觉的三种佛果",
  },
  {
    ruby: "gù zhī bō rě bō luó mì duō ， shì dà shén zhòu ， shì dà míng zhòu",
    text: "故知般若波罗蜜多，是大神咒，是大明咒",
    explain: "【解释】所以说心经，是变幻莫测的咒语，是神光普照的咒语",
  },
  {
    ruby: "shì wú shàng zhòu ， shì wú děng děng zhòu",
    text: "是无上咒，是无等等咒。",
    explain: "【解释】是无上的咒语，是最高的咒语",
  },
  {
    ruby: "néng chú yī qiē kǔ ， zhēn shí bù xū",
    text: "能除一切苦，真实不虚。",
    explain: "【解释】能除一切苦 ，不是骗人的",
  },
  {
    ruby: "gù shuō bō rě bō luó mì duō zhòu",
    text: "故说般若波罗蜜多咒。",
    explain: "【解释】所以说心经",
  },
  {
    ruby: "jí shuō zhòu yuē ， jiē dì jiē dì ， bō luó jiē dì",
    text: "即说咒曰：揭谛揭谛，波罗揭谛",
    explain: "【解释】其咒语曰：去吧，去吧，到彼岸去吧",
  },
  {
    ruby: "bō luó sēng jiē dì ， pú tí sà pó hē",
    text: "波罗僧揭谛，菩提萨婆诃。",
    explain: "【解释】大家快去彼岸，修成正果",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
  {
    ruby: "",
    text: "",
    explain: "",
  },
];
</script>

<style scoped></style>
