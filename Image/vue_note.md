# ����
[��Ƶ(�й��Vue2.0+Vue3.0ȫ�׽̳�حvuejs�����ŵ���ͨ)](https://www.bilibili.com/video/BV1Zy4y1K7SH/?spm_id_from=333.999.0.0&vd_source=56899dea646547051c5cf13d624feb11)
[�ĵ�(Vue�ٷ�)](https://v2.cn.vuejs.org/v2/guide/index.html)

# Vue��ʲô��
һ������**�����û�����**��**����ʽ**JavaScript���
���ݡ���>����
# Vue���ص�
1���������Vue(html css js)
![](/.vscode/note/ǰ��ѧϰ�ʼ�/Vue/vue01.png)
2.����ʽ����ԭ��JS������ʽ�γɶԱȣ�
3.ʹ��**����DOM+**�����**Diff�㷨**����������DOM�ڵ�
![](/.vscode/note/ǰ��ѧϰ�ʼ�/Vue/vue02.png)
# Vue�Ŀ�����������
1.���ؿ����汾
2.��װ�ȸ���
3.����ProductionTip�����ʾ����
![](image.png)
**Ϊʲô��ProductionTip��ֵ�ĳ���fales���ǳ�����ʾ��**
# ��ʶVue
## Helloʵ��
![](image-1.png)
**Ϊʲô����favicon.ico��ǩ���Ǳ���**
![](image-2.png)
�Ұѱ�ǩ�ŵ�Vue�ļ��������û�ã���ת����ԭ��λ�ã����ֱ���û����
�ܽ᣺
>1.����Vue�������ͱ��봴��һ��Vueʵ������Ҫ����һ�����ö���
2.root������Ĵ�����Ȼ����html�淶��ֻ����������һЩ�����Vue�﷨��
3.root������Ĵ��뱻��Ϊ[Vueģ��]��
4.Vueʵ����������һһ��Ӧ�ģ�
5.��ʵ������ֻ��һ��Vueʵ�������һ���������һ��ʹ�ã�
6.({xxx)}�е�xxxҪдjs���ʽ����xxx�����Զ���ȡ��ata�е��������ԣ�
7.һ��data�е����ݷ����ı䣬��ôģ�����õ������ݵĵط�Ҳ���Զ����¡�

ע�����֣�js���ʽ��js���루��䣩
>1,���ʽ��һ�����ʽ������һ��ֵ�����Է����κ�һ����Ҫֵ�ĵط���
(1)a
(2)a+b
(3)demo(1)
(4)X==y?'a':'b'
2.js���루��䣩
(1)if(){}
(2)for(){}
# ģ���﷨
>1.��ֵ�﷨��
���ܣ����ڽ�����ǩ�����ݡ�
д����{{xxx}},xxx��js���ʽ���ҿ���ֱ�Ӷ�ȡ��data�е��������ԡ�
2.ָ���﷨��
���ܣ����ڽ�����ǩ(��������ǩ���ԡ���ǩ�����ݡ����¼�����������)
������v-bind:href="xxx"���дΪ��href="xxx",xxxͬ��Ҫдjs���ʽ��
�ҿ���ֱ�Ӷ�ȡ��data�е��������ԡ�
��ע��Vue���кܶ��ָ�����ʽ���ǣ�v-???,�˴�����ֻ����v-bind�ٸ����ӡ�

exe:
~~~
<body>
    <!-- ׼��һ������ -->
    <div id="root">
        <!-- ��ֵ�﷨ -->
        <h1>Hello!{{name}}</h1>
        <!-- ָ���﷨ -->
        <a :href="url">����ѧϰģ���﷨</a>
    </div>
    <script>
        Vue.config.productionTip = false //����Ϊ false ����ֹ vue ������ʱ����������ʾ
        //����Vueʵ��
        new Vue(
            {
                el: '#root',//el����ָ����ǰVueʵ��Ϊ�ĸ���������ֵͨ��Ϊcssѡ�����ַ���
                data: { //data�����ڴ������ݣ����ݹ�elָ��������ȥʹ��
                    name: 'Lenovo',
                    url: "https://www.bilibili.com/video/BV1Zy4y1K7SH?p=7&spm_id_from=pageDriver&vd_source=56899dea646547051c5cf13d624feb11"
                }
            }
        )
    </script>
</body>

~~~
# ���ݰ�
>Vue����2�����ݰ󶨵ķ�ʽ��
1.�����(v-bind):����ֻ�ܴ�data����ҳ�档
2.˫���(v-model):���ݲ����ܴ�data����ҳ�棬�����Դ�ҳ������data.
��ע��
1,˫���һ�㶼Ӧ���ڱ���Ԫ����(�磺input��select��)
2.v-model:value���Լ�дΪv-model,��Ϊv-modelĬ���ռ��ľ���valueֵ��

exe
![](image-3.png)
# el �� data ������д��
**el**
![](image-4.png)
**data**
![](image-5.png)
��д
~~~
data(){
return{}
}
~~~
�ܽ�
>1.e1��2��д��
(1)new Vuelʱ������el���ԡ�
(2)�ȴ���Vueʵ���������ͨ��vm.$moun('#root')ָ��el��ֵ��
2.data��2��д��
(1)����ʽ
(2)����ʽ
���ѡ��Ŀǰ����д�������ԣ��Ժ�ѧϰ�����ʱ��data����ʹ�ú���ʽ������ᱨ��
3.һ����Ҫ��ԭ��
Vue����ĺ�����һ����Ҫд��ͷ������һ��д�˼�ͷ������this�Ͳ�����Vueʵ���ˡ�
# MVVMģ��
1.M:ģ��(Mode1):data�е�����
2.V:��ͼ(View):ģ�����
3.VM:��ͼģ��(ViewModel):Vueʵ��
![](image-6.png)
![](image-7.png)
�۲췢�֣�
1.data�����е����ԣ���󶼳�������vm���ϡ�
2.vm�������е����Լ�Vueԭ�����������ԣ���Vueģ���ж�����ֱ��ʹ�á�
# ���ݴ���
## �ع�Object.definneProperty����
~~~
 let number = 18
        let person = {
            name: '��ɽ',
            sex: '��'
        }
        Object.defineProperty(person, 'age', {
            // �����˶�ȡperson��age����ʱ��get������getter���ͻᱻ���ã��ҷ���ֵ����age��ֵ
            get: function () {
                // console.log('���˶�ȡage������')
                return number
            },
            //�������޸�personi��age����ʱ��set����(setter)�ͻᱻ���ã��һ��յ��޸ĵľ���ֵ
            set(value) {
                console.log("�����޸���age����,��ֵ��", value)
                number = value

            }
~~~
## Vue�е����ݴ���
>ͨ��vm����������data���������ԵĲ���(��/д)
2.Vue�����ݴ���ĺô���
���ӷ���Ĳ���data�е�����
3.����ԭ��
ͨ��Object.defineProperty������data����������������ӵ�vm�ϡ�
Ϊÿһ����ӵ�vm�ϵ����ԣ���ָ��һ��getter/setter��
��getter/setter�ڲ�ȥ����(��/д)data�ж�Ӧ�����ԡ�

![](image-9.png)
**�Դ�ͼ�ҵ����**
1.������д��data�е�����ʱ��vm�лḴ��һ�ݵ�_data�У����û�����ݴ���Ļ�����ʹ��{{}}ʱ������д��{{_data.name}}�ſ���ʹ�ã�
2.��Ϊ�����ݴ���_data������ݻ��ȡһ��ֱ����vm����Կ���ֱ����{{name}};
3._data������ݻ��ȡһ��ֱ����vm��,ʹ�õ���vm���grtter��������ģ������õ���setter��
# �¼�����
## �¼��Ļ���ʹ�ã�
>1.ʹ��v-on:xxx��@xxx���¼�������xxx���¼���;
2.�¼��Ļص���Ҫ������methods�����У����ջ���vm��;
3.methods�����õĺ�������Ҫ�ü�ͷ����������this�Ͳ���vm��;
4.methods�����õĺ��������Ǳ�Vue������ĺ�����this��ָ����vm�����ʵ������;
5.@click="demo����@click="demo(Sevent)"Ч��һ�£������߿��Դ���;
## �¼����η�

>1.prevent:��ֹĬ���¼������ã���
2.stop:��ֹ�¼�ð�ݣ����ã�;
3.once:�¼�ֻ����һ�Σ����ã�;
4.capture:ʹ���¼��Ĳ���ģʽ;
5.self:ֻ��event.target�ǵ�ǰ������Ԫ��ʱ�Ŵ����¼�;
6.passive:�¼���Ĭ����Ϊ����ִ�У�����ȴ��¼��ز�ִ�����;
## �����¼�
>1.Vue�г��õİ���������
����=>enter
���=>delet
(����ˢ�����͡��ٸ񡱽�)
�˳�=>
esc
�ո�=>space
����=>tab(���⣬�������keydownȥʹ��)
��=>up
��=>down
��=>1eft
��=>right
2.Vueδ�ṩ�����İ���������ʹ�ð���ԭʼ��keyֵȥ�㶨����ע��ҪתΪkebab-case���̺���������
3.ϵͳ���μ����÷����⣩��ctrl��a1t��shift��meta
(1)���kyupʹ�ã��������ν���ͬʱ���ٰ���������������ͷ����������¼��ŹĴ�����
(2)���keydownʹ�ã����������¼���
4.Ҳ����ʹ��keyCodeȥָ������İ��������Ƽ���
5.Vue,config.keyCodes,�Զ������=���룬����ȥ���ư�������
# ��������
�������ԣ�
1.���壺Ҫ�õ����Բ����ڣ�Ҫͨ���������Լ��������
2.ԭ���ײ������Objcet.defineproperty�����ṩ��getter��setter.
3.get����ʲôʱ��ִ�У�
(1)���ζ�ȡʱ��ִ��һ�Ρ�
(2)�����������ݷ����ı�ʱ�ᱻ�ٴε��á�
4.���ƣ���methodsʵ����ȣ��ڲ��л�����ƣ����ã���Ч�ʸ��ߣ����Է��㡣
5.��ע��
1.�����������ջ������vm�ϣ�ֱ�Ӷ�ȡʹ�ü��ɡ�
2.�����������Ҫ���޸ģ��Ǳ���дset����ȥ��Ӧ�޸ģ���set��Ҫ�������ʱ���������ݷ����ı䡣
**exe**
~~~
 <!-- ����һ������ -->
    <div id="root">
        �գ�<input type="text" v-model="firstName"><br>
        ����<input type="text" v-model="lastName"><br>
        ȫ����<span>{{fullName}}</span>
    </div>
    <script>
        Vue.config.productionTip = false //����Ϊ false ����ֹ vue ������ʱ����������ʾ
        const vm = new Vue({
            el: '#root',
            data: {
                firstName: '��',
                lastName: '��'
            },
            computed: {
                // fullName: {
                //     //                 get��ʲô���ã������˶�ȡfullNameʱ��get�ͻᱻ���ã��ҷ���ֵ����Ϊfu11Name��ֵ
                //     //                getʲôʱ����ã�1.���ζ�ȡfullNameʱ��2.�����������ݷ����仯ʱ��
                //     get() {
                //         return this.firstName + '-' + this.lastName
                //     },
                // }
                // �������Եļ�д
                fullName() {
                    return this.firstName + '-' + this.lastName
                }
            }
        })
    </script>
~~~
setter(������)
~~~
set(value){
console.log('set',value)
const arr = value.split('-')
this.firstName arr[0]
this.lastName arr[1]
//set��Ҫ�������ʱ���������ݷ����ı�
}
~~~
# ��������watch
1.�������ӵ����Ա仯ʱ���ص�����handler�Զ����ã�������ز���
2.���ӵ����Ա�����ڣ����ܽ��м��ӣ���
3.���ӵ�����д����
(1)new Vueʱ����watch����
~~~
Vue
watch:{
    info:{
    //
    }
}
~~~
(2).ͨ��vm.$watch����
~~~
vm.$watch('shuxing','watch��shuxing�������')
~~~
��ȼ��ӣ�
>(1).Vue�е�watchĬ�ϲ��������ڲ�ֵ�ĸı䣨һ�㣩��
(2).����deep:true���Լ������ڲ�ֵ�ı䣨��㣩��
��ע��
(1).Vue������Լ������ڲ�ֵ�ĸı䣬��Vue�ṩ��watchĬ�ϲ����ԣ�
(2).ʹ��watchʱ�������ݵľ���ṹ�������Ƿ������ȼ��ӡ�

��д
![](image-10.png)
![](image-11.png)
computed.��watch.֮�������
>1.computed����ɵĹ��ܣ�watch��������ɡ�
2,watch����ɵĹ��ܣ�computed��һ������ɣ����磺watch���Խ����첽������
������Ҫ��Сԭ��
1.����Vue����ĺ��������д����ͨ����������this��ָ�����vm�����ʵ������
2.���в���Vue������ĺ���(��ʱ���Ļص�������ajax�Ļص�������)�����д�ɼ�ͷ������
����this��ָ�����vm�����ʵ������
# ����ʽ
1.c1ass��ʽ
д����class="xxx"xxx�������ַ������������顣
�ַ���д�������ڣ�������ȷ����Ҫ��̬��ȡ��
����д�������ڣ�Ҫ�󶨶����ʽ��������ȷ��������Ҳ��ȷ����
����д�������ڣ�Ҫ�󶨶����ʽ������ȷ��������Ҳȷ��������ȷ���ò��á�
2.style��ʽ
:style="{fontsize:xxx}"����xxx�Ƕ�ֵ̬��
:style="[a,b]"����a��b����ʽ����
# ������Ⱦ
1.**v-if**
д����
(1).v-if="���ʽ"
(2).v-else-if="���ʽ"
(3).v-else="���ʽ"
�����ڣ��л�Ƶ�ʽϵ͵ĳ�����
�ص㣺��չʾ��D0MԪ��ֱ�ӱ��Ƴ���
ע�⣺v-if���Ժͣ�**v-else-if**��**v-else**һ��ʹ�ã���Ҫ��ṹ���ܱ�����ϡ���
2.**v-show**
д����V-show="���ʽ"
�����ڣ��л�Ƶ�ʽϸߵĳ�����
�ص㣺��չʾ��D0MԪ��δ���Ƴ���������ʹ����ʽ���ص�
3.��ע��ʹ��v-if��ʱ��Ԫ�ؿ����޷���ȡ������ʹ��v-showһ�����Ի�ȡ����
# �б���Ⱦ
## �����б�
��������--�������顢����
![](image-12.png)
**�ܽ�**
v-forָ��
1.����չʾ�б�����
2.�﷨��v-for="(item,index)in xxx"          :key="yyy"
3.�ɱ��������顢�����ַ������õĺ��٣���ָ���βأ��õĺ��٣�
## key��ԭ��
1.����D0M��key�����ã�
>key������DOM����ı�ʶ�������ݷ����仯ʱ��Vue����ݡ������ݡ�����[�µ�����DoM]�����Vue����[������DoM]��[������DoM]�Ĳ���Ƚϣ��ȽϹ�������;

2.�Աȹ���
>(1)������DOM���ҵ�����������DOM��ͬ��key:
a.������DOM������û�䣬ֱ��ʹ��֮ǰ����ʵDOM!
b.������DOM�����ݱ��ˣ��������µ���ʵDOM,����滻��ҳ����֮ǰ����ʵDOM.
(2)������DOM��δ�ҵ���������DOM��԰��key
�����µ���ʵDOM,�����Ⱦ����ҳ�档

3.��index��Ϊkey���ܻ����������⣺
>1.�������ݽ��У�������ӡ�����ɾ�����ƻ�˳�������
   �����û�б�Ҫ����ʵDOM����=>����Ч��û���⣬��Ч�ʵ͡�
2.����ṹ�л������������DOM:
    ���������DOM����==>���������⡣


4.���������ѡ��key?:
>1.���ʹ��ÿ�����ݵ�Ψһ��ʶ��Ϊkey,����id���ֻ��š����֤�š�ѧ�ŵ�Ψһֵ��
2.��������ڶ����ݵ�������ӡ�����ɾ�����ƻ�˳���������������Ⱦ�б�����չʾ��ʹ��index��ΪKey��û������ġ�

**�����б�ʱkey������(id��Ϊkey)**
![](image-13.png)
**�����б�ʱkey������(index��Ϊkey)**
![](image-14.png)

## �б����
watch����
~~~
vue
<body>
    <div id="root">
        <input type="text" placeholder="����������" v-model="keyWord">
        <ul>
            <li v-for="p of filPersons">
                {{p.name}}
            </li>
        </ul>
    </div>
    <script>
        Vue.config.productionTip = false
        const vm = new Vue({
            el: '#root',
            data: {
                keyWord: '',
                persons: [
                    { name: "���" },
                    { name: "��Сǿ" },
                    { name: "��ǿ׳" },
                    { name: "�ܴ���" }
                ],
                filPersons: []
            },
            watch: {
                keyWord: {
                    immediate: true,
                    handler(val) {
                        this.filPersons = this.persons.filter((p) => {
                            return p.name.indexOf(val) !== -1
                        })
                    }
                }
            }



        })

    </script>
</body>

~~~
computed����
~~~
vue
            computed: {
                filPersons() {
                    return filPersons = this.persons.filter((p) => {
                        return p.name.indexOf(this.keyWord) !== -1
                    })
                }

            }
~~~
## �б�����
~~~
vue
<body>
    <div id="root">
        <input type="text" placeholder="����������" v-model="keyWord">
        <button @click="sortType=2">��������</button>
        <button @click="sortType=1">���併��</button>
        <button @click="sortType=0">ԭ˳��</button>
        <ul>
            <li v-for="p of filPersons">
                {{p.name}}--{{p.age}}
            </li>
        </ul>
    </div>
    <script>
        Vue.config.productionTip = false
        const vm = new Vue({
            el: '#root',
            data: {
                keyWord: '',
                sortType: 0,//0ԭ˳�� 1���� 2����
                persons: [
                    { name: "���", age: 23 },
                    { name: "��Сǿ", age: 7 },
                    { name: "��ǿ׳", age: 46 },
                    { name: "�ܴ���", age: 22 }
                ]
            },
            computed: {
                filPersons() {
                    const arr = this.persons.filter((p) => {
                        return p.name.indexOf(this.keyWord) !== -1
                    })
                    if (this.sortType) {
                        arr.sort((p1, p2) => {
                            return this.sortType === 1 ? p2.age - p1.age : p1.age - p2.age
                        })
                    }
                    return arr
                }

            }



        })

    </script>
</body>

~~~
# Vue�������
## ����������ʱ��һ������
~~~
Vue
method:{
    updataM:{
        this.person.name = xx, //��Ч
        this.person = [xx] //��Ч
    }
}
~~~
## Vue������ݵ�ԭ��_����
~~~
Vue
Vue.set(vm._data.sx,'xx','x')
~~~
## Vue������ݵ�ԭ��_����
~~~
Vue
vm._data.arr.push('xxx')
//shift.......
~~~
## Vue�������ݵ�ԭ���ܽ�
1.vue�����data�����в�ε����ݡ�
2.��μ������е����ݣ�
>ͨ��setterʵ�ּ��ӣ���Ҫ��new Vueʱ�ʹ���Ҫ�������ݡ�
(1)�����к�׷�ӵ����ԣ�VueĬ�ϲ�����Ӧʽ����
(2)���������ӵ���������Ӧʽ����ʹ������API:
Vue.set(target,propertyName/index,value)
��
vm.$set(target,propertyName/index,value)


3.��μ�������е����ݣ�
>ͨ�������������Ԫ�صķ���ʵ�֣����ʾ������������£�
(1).����ԭ����Ӧ�ķ�����������и��¡�
(2).���½���ģ�壬��������ҳ�档

4.��Vue�޸������е�ĳ��Ԫ��һ��Ҫ�����·�����
>1.ʹ����ЩAPI:push������pop������shift������unshift������splice������sort������reverse����
2.Vue.set����vm.$set����
�ر�ע�⣺Vue.set������vm.$set�������ܸ�vm��vm�ĸ����ݶ���������ԣ�

���̸��򵥵�deom
![](image-16.png)
~~~
Vue
<body>
    <div id="root">
        <h1>ѧ����Ϣ</h1>
        <button @click="student.age++">����+1</button><br />
        <button @click="addSex">����Ա����ԣ�Ĭ��ֵ����</button><br />
        <button @click="updataSex">�޸��Ա�</button><br />
        <button @click="addFriend">���б���λ���һ������</button><br />
        <button @click="updataFristfriend">�޸ĵ�һ�����ѵ�����Ϊ:Saral</button><br />
        <button @click="addHobby">���һ������</button><br />
        <button @click="updataHobby">�޸�һ������Ϊ����</button><br />
        <!-- <button>���˵������еĳ���</button><br /> -->
        <h2>����:{{student.name}}</h2>
        <h2 v-if="student.sex">�Ա�{{student.sex}}</h2>
        <h2>����:{{student.age}}</h2>
        <h2>����:</h2>
        <ul>
            <li v-for="(h,index) in student.hobby" :key="index">
                {{h}}
            </li>
        </ul>
        <h2>������:</h2>
        <ul>
            <li v-for="(f,index) in student.friends" :key="index">
                {{f.name}}--{{f.age}}
            </li>
        </ul>
    </div>
    <script>
        Vue.config.productionTip = false //����Ϊ false ����ֹ vue ������ʱ����������ʾ
        const vm = new Vue({
            el: '#root',
            data: {
                student: {
                    name: 'tom',
                    age: 18,
                    hobby: ['����', '�Ⱦ�', '��ͷ'],
                    friends: [
                        { name: "Jerry", age: 35 },
                        { name: "Tony", age: 36 }
                    ]
                }
            },
            methods: {
                addSex() {
                    Vue.set(this.student, 'sex', '��')
                },
                updataSex() {
                    this.student.sex = 'Ů'
                },
                addFriend() {
                    this.student.friends.unshift({ name: "Judy", age: 32 })
                },
                updataFristfriend() {
                    this.student.friends[0].name = 'Saral'
                },
                addHobby() {
                    this.student.hobby.push('ѧϰ')
                },
                updataHobby() {
                    this.student.hobby.splice(0, 1, '����')
                }
            },


        })
    </script>
</body>
~~~
# �ռ�������
����
![](image-17.png)
**�ܽ�**
>����< input type="text"/>,��v-model�ռ�����valueֵ���û�����ľ���valueֵ��

>����< input type:="radio"/>,��v-model�ռ�����valueֵ����Ҫ����ǩ����valueֵ��

>����< input type="checkbox"/>
1.û������input��value/���ԣ���ô�ռ��ľ���checked(��ѡorδ��ѡ���ǲ���ֵ)
2.����input��value���ԣ�
(1)v-model�ĳ�ʼֵ�Ƿ����飬��ô�ռ��ľ���checked(��ѡorδ��ѡ��
�ǲ���ֵ��
(2)v-mode1�ĳ�ʼֵ�����飬��ô�ռ��ĵľ���value��ɵ�����


��ע��v-model���������η���
>1azy:ʧȥ�������ռ�����
number:�����ַ���תΪ��Ч������
trim:������β�ո����

# ������
**����**����Ҫ��ʾ�����ݽ����ض���ʽ��������ʾ��������һЩ���߼��Ĵ���
**�﷨**��
>1.ע���������Vue.filter(name,cal1back)��new Vue{filters:{)}
2.ʹ�ù���������xxx|��������}��v-bind:����="xxx|��������"

**��ע**��
>1.������Ҳ���Խ��ն�����������������Ҳ���Դ���
2.��û�иı�ԭ�������ݣ��ǲ����µĶ�Ӧ������

# ָ��
## ����ָ��
v-bind������󶨽������ʽ���ɼ�дΪXXX
v-model:˫�����ݰ�
v-for����������/����/�ַ���
v-on�����¼��������ɼ�дΪ@
v-if��������Ⱦ����̬���ƽڵ��Ƿ����ڣ�
v-else��������Ⱦ����̬���ƽڵ��Ƿ����ڣ�
v-show��������Ⱦ����̬���ƽڵ��Ƿ�չʾ��
v-textָ�
>1.���ã��������ڵĽڵ�����Ⱦ�ı����ݡ�
2.���ֵ�﷨������v-text���滻���ڵ��е����ݣ�(xx)}�򲻻ᡣ

v-htmlָ�
>1.���ã���ָ���ڵ�����Ⱦ����html�ṹ�����ݡ�
2.���ֵ�﷨������
(1).v-htm1���滻���ڵ����е����ݣ���xx}�򲻻ᡣ
(2).v-html����ʶ��html�ṹ��
3.����ע�⣺v-html�а�ȫ�����⣡������
(1).����վ�϶�̬��Ⱦ����HTML�Ƿǳ�Σ�յģ����׵���**XSS����**��
(2).һ��Ҫ�ڿ��ŵ�������ʹ��v-html,����Ҫ�����û��ύ�������ϣ�

**����cookie**
![](image-18.png)

v-c1oakָ�û��ֵ����
>1.������һ���������ԣ�Vueʵ��������ϲ��ӹ������󣬻�ɾ��v-c1oak���ԡ�
2.ʹ��css���v-c1oak���Խ��������ʱҳ��չʾ��(xxx)�����⡣

v-onceָ�
>1.v-once���ڽڵ��ڳ��ζ�̬��Ⱦ�󣬾���Ϊ��̬�����ˡ�
2.�Ժ����ݵĸı䲻������v-once���ڽṹ�ĸ��£����������Ż����ܡ�

v-preָ�
>1.���������ڽڵ�ı�����̡�
2.��������������û��ʹ��ָ���﷨��û��ʹ�ò�ֵ�﷨�Ľڵ㣬��ӿ���롣

## �Զ���ָ��
�����﷨��
>(1).�ֲ�ָ�
new Vue({
directives:{ָ���������ö���}
})
��
new Vue({
directives{ָ�������ص�����}
})
(2).ȫ��ָ�
Vue.directive(ָ���������ö���)
��
Vue,directive(ָ�������ص�����)


���ö����г��õ�3���ص���
>(1).bind:ָ����Ԫ�سɹ���ʱ���á�
(2).inserted:ָ������Ԫ�ر�����ҳ��ʱ���á�
(3).update:ָ������ģ��ṹ�����½���ʱ���á�

������ע��
>1,ָ���ʱ����V-,��ʹ��ʱҪ��V-:
2,ָ��������Ƕ�����ʣ�Ҫʹ��kebab-case������ʽ����Ҫ��camelCase������
