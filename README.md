# 表单设计器 beta

## 安装依赖
``` 
# 使用yarn 
yarn add k-form-design

# 使用npm 
npm install k-form-design -S
```

### 引入
``` 
在main.js引入

import { KFormDesign, KFormBuild } from "k-form-design";

Vue.use(KFormDesign);
Vue.use(KFormBuild);
```

### 设计器使用
``` 
<template>
  <div>
    <k-form-design @handleSave="handleSave" />
  </div>
</template>
<script>
export default {
  methods: {
    handleSave(val) {
      this.$message.success("触发保存方法");
      console.log(val);
    }
  }
};
</script>
```
### 解析器使用
``` 
// jsonData 设计器生成的json数据
<k-form-build
      :value="jsonData"
      ref="KFormBuild"
      @submit="handleSubmit"
    />
```

![1.jpg](https://i.loli.net/2019/09/29/X2h9Kji5HpC6ZdB.png)
![2.jpg](https://i.loli.net/2019/09/29/OzBGS6F2ZmflMCw.png)
![3.jpg](https://i.loli.net/2019/09/29/oYOjwT3qUr2SMmA.png)
![4.jpg](https://i.loli.net/2019/09/29/JtCDZELxe3r5ARl.png)
![5.jpg](https://i.loli.net/2019/09/29/NTGmdoDPXvqHJMe.png)