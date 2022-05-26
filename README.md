# Learn-javascripts

# let & const

let(variable values): 값을 수정할 수 있는 변수를 선언할 때 사용<br>
const(constant values): 값을 수정하지 않을 때 사용<br>

<br>

# Arrow Functions

    function myFnc(){
        ...
    }

    const myFnc = () => {
        ...
    }
    * No more issues with the 'this' keyword
<br>

# Expors & Imports (Modules)

* person.js 

        const person = {
            name:'Max'
        }

        export default person
<br>

* utility.js

        export const clean = () =>{
            ...
        }

        export const baseData = 10;

<br>

* app.js 

        // default export 
        import person from './person.js'
        import prs from './person.js'
        
        // named export: 이름으로 참조, 중괄호 사용, import * 사용 가능
        import {clean, baseData} from './utility.js'

<br>

# Classes

<br>

* Class

        class Person{
            constructor(){
                this.name = 'Max'
            }
            //name = 'Max' 로 직접 선언해도 constructor에 선언한 것과 같다.

            call = () =>{
                console.log(this.name)
            }
        }
<br>

* Usage

        const myPerson = new Person()
        myPerson.call()
        ...
<br>

* Inheritance

        class Person extends Animal {
            constructor(){
                super(); // 상속을 받았다면 super()함수 호출
                this.name='Max'
            }
            ...
        }

<br>

# Spread & Rest Operators

- Spread ...

        const newArray = [...oldArray]
        const newObject = {...oldObject}

<br>

- Rest

        function sortArgs(...args){
            ...
        }

        //모든 parameter를 배열로 통합한다.

 
 <br>

 # Destructuring

 <br>

 - Array Destructuring

        [a,b] = ['Hello', 'Max']

<br>

- Object Destructuring

        {name} = {name:'Max', age:28}

<br>

# Array Function

    const numbers = [1, 2, 3, 0];
<br>

- map
        
        const doubleNumArray = numbers.map((num)=>{
            return num * 2;
        });

        //result: [1, 4, 6]
<br>

- find: 조건에 맞는 요소 중 가장 먼저 있는 값을 반환

        const found = numbers.find(element => element > 1);

        //result: 1
<br>

- findIndex: 조건에 맞는 요소 중 가장 먼저 있는 인덱스 반환

        const foundIndex = numbers.findIndex(
            (element) => element > 2
        );

        //result: 2

<br>

- filter: 조건에 맞는 값 전부를 배열로 반환

        const filterArray = numbers.filter((num) => num > 1);

        //result: [2, 3]

<br>

- slice: 배열 자르기

        numbers.slice(1); //[1, 2]
        numbers.slice(1, 2); //[2, 3]
        number.slice(-1); //[0]

<br>

- splice: 배열 치환

        numbers.splice(1, 0, 10) // [1, 10, 3, 0] 인덱스 1에 10 삽입
        numbers.splice(1, 2, 30) // [1, 30, 0] 1 ~ 2까지 30으로 치환