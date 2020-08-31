#	TypeScript-Study

<details>
    <summary>ESNext 중요 문법 정리</summary>
    <div markdown="1">

    ## ESNEXT(ECMAScript2015~2019) 중요 문법 정리

    1. 비구조화 할당

    ``` javascript
    //비구조할당
    let person = {name: "minje", age: 24}
    let {name, age} = person
    
    //비구조할당, 잔여연산자
    let array = [1,2,3,4]
    let [head, ...rest] = array //head = 1, rest = [2,3,4]
    ```

    비구조화 할당을 통해 각 맵버를 쉽게 얻을 수 있다.

    2. 화살표 함수

    ``` javascript
    function add(a, b) {return a + b}
    const add = (a, b) => a + b
    ```

    화살표 함수를 이용하면 코드를 간결하게 작성 할 수 있다

    3. 클래스

    ``` javascript
    abstract class Animal{
        constructor(public name?: string, public age?:number)
        abstract say(): string
    }
    class Cat extends Animal{
        say(){return '야옹'}
    }
    class Dog extends Animal{
        say(){return '멍멍'}
    }
    let animals: Animal[] = [new Cat('고양이', 3), new Dog('강아지', 1)]
    let sounds = animals.map(a => a.say())
    ```

    4. 모듈

    ``` javascript
    export default function a()
    import a from 'a'
    
    export function a()
    import { a } from 'a'
    ```

    5. 생성기

    ``` javascript
    function* gen(){
        yield* [1,2]
    }
    for(let value of gen()) console.log(value) //1, 2
    ```

    생성기는 function*과 yield 키워드를 이용해 만든다.

    6. promise와 async/await 구문

    ``` javascript
    async function get(){
        let values = []
        values.push(await Promise.resolve(1))
        values.push(await Promise.resolve(2))
        values.push(await Promise.resolve(3))
        return values
    }
    
    get().then(values => console.log(values)) // [1,2,3]
    ```

    async 사용한 함수는 await 키워드를 사용할 수 있다. await는 Promise 객체를 해소해 get함수에 [1,2,3] 값을 Promise 형태로 반환 한다.

    get함수가 반환한 Promise객체는 then 메서드로 실제값을 얻을 수 있다.

    7. 삼항연산자

    ``` javascript
    const a = fasle
    
    a ? console.log("진실") : console.log("거짓") // 거짓
    
    const a = 10
    
    a == 10 ? console.log("진실") : console.log("거짓") // 진실
    ```

    삼항연산자는 의외로 사용되는 곳들이 많고 사용법도 쉽다.

   

   </div>
</details>

<details>
<summary>개발환경 구성</summary>
<div markdown="2">

## 시작하기전 환경구성 부터 해보자..

 1. 비주얼 스튜디오 코드 설치

    마이크로소프트에서 받자.

 2. NodeJs 설치
    
    nodejs 홈페이지서 받자.

 3. 타입스크립트 컴파일러 설치

    ``` Terminal
    > npm i -g typescript

    > tsc -v
    Version 4.0.2(20-08-31기준) //에러없이 설치되었다면 정상적으로 버전이 확인 가능.

    > tsc ./2020-08-31/hello.ts
    //2020-08-31폴더에 hello.js 파일이 생성되는 것 확인.

    > node ./2020-08-31/hello.js
    // hello world!
    ```

 4. ts-node 설치

    ts-node는 타입스크립트 코드를 ES5 형식의 자바스크립트 코드로 변환하고, 동시에 실행까지 해준다.

    즉 3번에 tsc로 컴파일후 node로 실행 과정을 ts-node로 한번에 가능하다.

     ``` Terminal
    > npm i -g ts-node

    > ts-node ./2020-08-31/hello.ts
    // hello world!
     ```
</div></details>


</details>