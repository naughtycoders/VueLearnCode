<template>
    <h4>列表渲染</h4>
    <P v-for="(item,index) in names" :key="index">{{ item }}-{{ index }}</P>
    <div v-for="web in result">
        
        <p :class=web.dynamicclass :key="web.id">{{ web.title }}</p>
        <a :href='web.avator'>{{ web.title }}</a>
        
    </div>
    <p v-for="(value, key, index) in userInfo">{{ value }}-{{ key }}-{{ index }}</p>
    <!-- <p v-for="web in result" v-bind="web">{{ web['title'] }}</p> -->
</template>

<script>
    export default{
        data() {
            return {
                names: ['百战程序员', '尚学堂', 'IT'],
                result:[
                    {
                        "id": 123456,
                        "title": '百度',
                        dynamicclass: 'appclass1',
                        'avator': 'https://www.baidu.com/'
                    },
                    {   
                        'id': 234567,
                        'title': '淘宝',
                        dynamicclass: 'appclass2',
                        'avator': 'https://www.taobao.com'
                    },
                    {   
                        'id': 345678,
                        'title': '京东',
                        dynamicclass: 'appclass3',
                        'avator': 'https://www.jd.com'
                    }
                ],
                userInfo:{
                    name:'jack',
                    age:20,
                    sex:'男'
                }
            }
        }
    }
</script>