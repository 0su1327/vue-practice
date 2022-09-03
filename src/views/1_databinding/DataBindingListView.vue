<template>
    <div>
        <div>
            <select name="" id="">
                <option :value="city.code" :key="city.code" v-for="city in cities">{{city.title}}</option>
            </select>
        </div>
        <div>
            <table>
                <thread>
                    <tr>
                        <th> id |</th>
                        <th> 아파트 명 |</th>
                        <th> 이름 |</th>
                        <th> 전화번호 |</th>
                    </tr>
                </thread>
                <tbody>
                    <tr :key="apart.id" v-for="apart in apartment">    <!--i는 index를 의미한다.  가로채우는 행위를 list갯수만큼 하면 되므로 tr을 v-for만큼 돌린다. -->
                        <td>{{ apart.id }}</td>
                        <td>{{ apart.name }}</td>
                        <td>{{ apart.phoneNumber }}</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '064' }
      ],
      apartment: [
        {
          id: '1',
          apartment: '행복아파트',
          name: '홍길동',
          phoneNumber: '01012341234'

        },
        {
          id: '2',
          apartment: '복행아파트',
          name: '홍동',
          phoneNumber: '01000001234'

        },
        {
          id: '3',
          apartment: '행복아파트',
          name: '나영수',
          phoneNumber: '01094561234'

        },
        {
          id: '4',
          apartment: '안행복아파트',
          name: '홍길동',
          phoneNumber: '01078945612'

        },
        {
          id: '5',
          apartment: '이이아파트',
          name: '홍길동',
          phoneNumber: '01015641564'

        }
      ]
    }
  },
  setup() {},
  created() {},
  mounted() {},
  methods: {}
}
</script>

<style>
    table{
    width: 75%;
    text-align : left;
    }
    tanle th{
        padding : 12px;
        border-bottom: 2px solid  darkgray;
    }
    table td{
        padding : 12px;
    }
    table tr:nth-of-type(even){
        background-color: rgba(0,0,255,0.1);
    }
</style>
