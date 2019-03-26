<template>
  <view class="container">
    <flat-list
      class="main-list"
      :data="[{title: 'Baked Pizza', recs: 43, key:'0'}, {title: 'The Beanhive', recs: 10, key:'1'}]"
      :render-item="(item) => renderList(item)">
  </view>
</template>

<script>
  import React from 'react';
  import {Text, View} from 'react-native';
  export default {
    methods: {
      renderList: function(item) {
        return (
          <View class="item-container"
            style={{paddingLeft:8, borderColor:"#000", borderBottomWidth: 2, borderTopWidth: 2}}>
            <Text
              style={{marginBottom:30, marginTop:10}}>
              {item.item.title} {item.item.recs} people reccomend this space
            </Text>
          </View>
        )
      }
    }
  }
</script>

<style>
.container {
  background-color: white;
  flex: 1;
}
.main-list {
  margin-top: 30;
}

.list-item {
  color:red;
}

</style>
