### TypeScript 정리전 ESNEXT(ECMAScript2015~2019)문법 정리

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

   화살표 함수를 이용하면 코드를 간결하게 할 수 있고, 매개변수가 없을시 ()까지 생략하여 사용이 가능하고, return도 생략가능하다.

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
export default function a()
import a from 'a'

export function a()
import { a } from 'a'
```

자바스크립트의 종류는 ECMAScript, ESNext(ECMAScript 2015~2019), TypeScript가 있고 서로의 상관 관계를 나타내면



ECMAScript < ESNext(ECMAScript 2015~2019) < TypeScript 라고 볼 수 있다.

