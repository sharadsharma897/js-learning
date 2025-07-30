# js-learning
js-learning

1. == and >,<,>=,<= are different, ex (null > 0) false, (null == 0) false, (null >=0) true, in later 4 null will be converterd as 0.
but for undefined , all will be false

=== strict check ("2" == 2) true but ("2" === 2) false, check both value and type
null means empty

2. premitive (call by value), string, number, boolean,null, undefined(variable declared, not assigned), symbol, BigInt
3. reference type( non premitive), Array, Object, Functions
4.type of null is object, type of function is function
5. const a = [1,2,3,4,5] , a.join(), will convert array intp string
6. slice will not change original array, splice will remove the slice portion from original array
7. object declared as litrels in not sigleton, but through constructer (Object.create
8. function addNumbers(...num){  // here ... is rest operator, outcome is [200,300,400]
  return num
}
console.log(addNumbers(200,300,400))

9. const user = {
    username:"Sharad",
    price: 100,
    welcomeMessage : function(){
        console.log(`welcome: ${this.username}`)
        console.log(this);
        
    }
}
user.welcomeMessage()
user.username = "sam"
user.welcomeMessage()   //this.username This will here.

BUT here in function its undefined
function chai(){
    let username = "Sharad"
    console.log(this.username) // this will result into undefined
    //console.log(this);
    
}

chai()

10.  console.log(this); will give lot of stuff , but arrow function will give {} as outcome
function chai(){
    let username = "Sharad"
    //console.log(this.username)
    console.log(this);
    
}

chai()

const chai1 = () => {
     let username = "Sharma"
     //console.log(username)
     console.log(this);
     
}

chai1()

11. implecit return  ex  const addTwo = (num1, num2) => num1+num2
    or  const addTwo = (num1, num2) => (num1+num2) ,

    so if {} used then we havd to write return

    if we have to return object, that need to be inclosed in () ex  const addTwo = (num,num2) => ({ name:"sharad"})

12. Immediately invoked function Expressions ( IIFE) // it is used to avoid polution due to global variables
(function chai(){
    console.log("hello from IIFE..")
})();

(()=>
    console.log("hello from IIFE....")
)()

13. Java script Execution context, means how java script run your js file. note: js is single threaded
  - Global EC , allocates to this
  - function execution context
  - Eval EC
phases:
-memory ceation phase
-execution phase

14. falsy ==> false,0,-0,BigInt 0n, null, undefined, NaN, except all are truethy like "0", 'fasle' (bcoz these two are string), object, function(){}, []
15. false == 0, false == '', 0 =='' all are true
16. Nullish coalescing Operator (??): null undefined

     let val1;
     val1 = 5 ?? 10 // if we print, value would be 5
    val1 = null ?? 10 // 10
    val1 = undefined ?? 15 // 15
    val1 = null ?? 10 ?? 15 // 15

17. For of  // array of onject case [{},{},{}]
    const arr = [1,2,3,4,5]
    for (const element of arr) {
    console.log(element);    
    }
18 map , Map object holds key value pairs and remembers the original insersion order of keys ( no duplicate values)

const map = new Map();
map.set("1","11111");
map.set("2","2222")

//console.log(map);

for(const [k,v] of map){
    console.log(k, '-', v)
}
