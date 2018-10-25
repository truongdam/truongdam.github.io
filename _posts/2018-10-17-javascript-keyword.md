---
layout: post
title: Javascript keywords
comments: true
---

## Important keywords in Javascript


There are important keywords, if you're senior developer you may already know, if you're a beginner you should find out about it:
- Javascript Engine: Google V8, SpiderMonkey
- Execution Context: Global Execution Context, Local Execution Context
- Call Stack
- Global Memory

[Visualize Javascript code executions](http://latentflip.com/loupe/)
- == vs === vs typeof

{% highlight text %}

    1 == "1" //true
    1 === "1" //false
    typeof {} //object
    typeof "String" //String
{% endhighlight %}
    
- Value Types, Reference Types
    - Value Types: String, Number, undefined, Boolean, null
    - Reference Types: Object, Array, Function 
- Lexical Scope, Function Scope, Block Scope
- Expression, statements, function declaration, function expression, named function expression
    - Expression: javascript code snippets that result in a single value.
    - Statements: if-else, while, do-while, for, switch, for-in, with, variable declaration

{% highlight text %}

    1 == "1"    //expression
    1 + 2 * 3   //expression
    true && isExactly()     //expression
    functionCall()      //expression
    
    if (true) {     //statements
        a = 1+1;
    }
{% endhighlight %}
    
   
   - funcion declaration, function expression, named function expression
   - Resource: [link](https://medium.com/@raviroshan.talk/javascript-function-declaration-vs-expression-f5873b8c7b38)
   
{% highlight text %}

    //function declaration
    function getPoint(){
        return [1, 1];
    } 
    
    //function expression 
    var getPoint = function(){
        return [1, 1];
    }
    
    //named function expression
    var addVariable = function addFunction(param1, param2) {
       var res = param1 + param2;
       if (res === 30) {
            res = addFunction(res, 10);
       }
       return res;
    }    
    
    
{% endhighlight %}

- IIFE, Modules, Namespaces
   - [Javascript modules, module formats, module loaders and module bundlers](https://www.jvandemo.com/a-10-minute-primer-to-javascript-modules-module-formats-module-loaders-and-module-bundlers/)
   - Message Queue and Event Loop

- Dom and Layout Trees
    - Render tree: DOM and CSSOM, combine the DOM and CSSOM into a render tree, run layout on the render tree
- Factories and Classes
 
{% highlight text %}

    //ES5: class Hero
    function Hero(name, level) {
        this.name = name;
        this.level = level;
    };
    
    Hero.prototype.greet = function(){
        return '${this.name} says Hello.';
    }
    
    //ES5: class Mage extends Hero
    function Mage(name, level, spell) {
        Hero.call(this, name, level);
        this.spell = spell;
    }
    //Note: class Mage don't has function greet()
    
    
    //ES6: class Hero
    class Hero {
        constructor(name, level) {
            this.name = name;
            this.level = level;
        }
    
        // Adding a method to the constructor
        greet() {
            return `${this.name} says hello.`;
        }
    }

    class Mage extends Hero {
        constructor(name, level, spell) {
            // Chain constructor with super
            super(name, level);
    
            // Add a new property
            this.spell = spell;
        }
    }
    //Note: class Mage don't has function greet()
        
{% endhighlight %}

- this, call, apply, bind
    - Function.prototype.call()
    - Function.prototype.apply()
    - Function.prototype.bind()

{% highlight text %}
    
    var obj = { name: 'Truong Dam'};
    var greeting = function(a, b){
        return 'welcome ' + this.name + ' to' + a + ' at ' + b; 
    }
    
    console.log(greeting.call(obj, 'hcm city', '2018));     // function.prototype.call()
    console.log(greeting.apply(obj, ['hcm city','2018']);   // function.protorype.apply()
    
    var bound = greeting.bind(obj);  // function.prototype.bind()
    console.log(bound('hcm', '2018');

{% endhighlight %}

 - Object.create, Object.assign
 
 {% highlight text %}

    var obj = { 
        name: "truong dam",
        printIntro : function() {
            console.log('My name is ${this.name}. I live at ${this.city} ');
        }
    };
    
    var copyObj = Object.create(obj);
    copyObj.city = 'hcm';
    copyObj.printIntro();
    
    
    var asObj = Object.assign({class:'economic', age: '22'}, obj);
    console.log(asObj.class, asObj.age, asObj.name);

 {% endhighlight %
 
- Map, filter, reduce
    [link](https://blog.codeanalogies.com/2018/07/24/javascripts-reduce-method-explained-by-going-on-a-diet/)

- Pure function, side effects, state mutation
- Closure
- Promise
    - [javascripts promises for dummies](https://scotch.io/tutorials/javascript-promises-for-dummies)

{% highlight text %}
    
    var isMove = false;
    
    var willMoveCity = new Promise( function(resolve, reject){
        
        if (isMove){
            var destination = {
                city : 'hcm',
                time: 2018
            };
            
            resolve(destination);
            
        } else {
            var reason = new Error('family don't move');
            reject(reason);
        
        }
        
    
    });
    
{% endhighlight %}

 

