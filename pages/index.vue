<template>
  <div>
    <b-button v-b-toggle.collapse-root variant="primary">壊魔守護</b-button>
    <b-collapse id="collapse-root" class="mt-2">
      <b-card>
        壊魔守護 =
        <b-button v-b-toggle.collapse-1s size="sm">恐魔守護</b-button> 継
        <b-button v-b-toggle.collapse-1a size="sm">壊クリソ</b-button> + X
        <b-collapse id="collapse-1s" class="mt-2">
          <b-card id="1s">
            恐魔守護 =
            <b-button v-b-toggle.collapse-21s size="sm">伝魔守護</b-button> 継
            <b-button v-b-toggle.collapse-21a size="sm">恐クリソ</b-button>
            {{ 剣21M }}
            <b-collapse id="collapse-21s" class="mt-2">
              <b-card id="21s">{{ 伝魔守護 }}</b-card>
            </b-collapse>
            <b-collapse id="collapse-21a" class="mt-2">
              <b-card id="21a">{{ 恐クリソ }} {{ 剣21M }}</b-card>
            </b-collapse>
          </b-card>
        </b-collapse>
        <b-collapse id="collapse-1a" class="mt-2">
          <b-card id="1a">
            壊クリソ =
            <b-button v-b-toggle.collapse-22s size="sm">恐クリソ</b-button> 継
            <b-button v-b-toggle.collapse-22a size="sm">壊ロイソ</b-button> + X
            <b-collapse id="collapse-22s" class="mt-2">
              <b-card id="22s">{{ 恐クリソ }} {{ 剣21M }}</b-card>
            </b-collapse>
            <b-collapse id="collapse-22a" class="mt-2">
              <b-card id="22a">拾う</b-card>
            </b-collapse>
          </b-card>
        </b-collapse>
      </b-card>
    </b-collapse>
  </div>
</template>

<script>
export default {
  data() {
    return {
      恐クリソ: `恐クリソ = ((伝ニンソ 合 マスソ = 伝クリソ) 継 恐ロイソ`,
      剣21M: ` + 21M剣 (宿神魔)`,
      伝魔守護: `伝魔守護 = 魔魔守護 継 伝クリソ x 2 + 10M剣 (魔神魔)`
    }
  }
}
</script>
