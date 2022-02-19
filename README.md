## TypeScript Simple Key-word-tips

## Type Build-in Types
```TypeScript
   const Name:'Rajan'
   let Name:'Rajan'
```
## Other Types 
Void
null
Undefined
Never -it's never return value 
Any  -it's support any data type

### Examples: 
```TypeScript
 let Name:string='rajan'
 let Name:string='rajan';
 let Name:string | null | Undfined ='rajan';
```

## Union types 

### Examples:
```TypeScript
let Name: number | string; -it's support string and number 
let Name: string | Null
```

## Type Assertion /Casting ;

### Examples: 
```TypeScript
 let age: any =50;
 let convetstring : String=(age as number).toFixed(3) //casting

typeof -> -- To help to identify the types
typeof(age)=
```
## Type Script Function 


## Examples: 
* Normal JavaScript Function 
```TypeScript
  function fun(age:number,name:string):string 
   {
   return 'hi'
   }
 * Optional parameter 
    function fun(age?number,name?:string):string 
     {
       return 'hi'
     }
```
 * Default value for the parameter 
```TypeScript
    function fun(age?number,name:string='rajan'):string 
     {
       return 'hi'
     }

    function fun(age:number,name?:string):Never  // It's never return any values
    {
       return 5
    }
```

## Arrow function 

    Left side parameter and right Function body 
	 Parmeter => Function body 
### Examples: 
  
```TypeScript
    1. Single parameter
       let square= x=> x* X; 
       let result =square(7);// it's return 49

    2. Multiple parameter

      let add =(a,b)=>a+b;
      let result =add(7,7); // it's return 14
  
    3. Without Parameter

	 let appname =() => return "Test TSC App"  

    4. function with Data annotation 

	  let test =(a:number,b:number):number => a + b;
 ```
 ## Type Script Custom Types

   ### Interface
   ```TypeScript    
	      interface ITest 
		   {
			   Name:string;
			   Age :number;
		   }
```
       Interface with inheritance
   ```TypeScript    

	   interface INewTest extends ITest
	    {
			GroupName:string;
			Country :string;
			GetValue : (value:string)=>string; // Method Declaration
	    }
 ```
		Type Script Structural type system
   ```TypeScript   
		   let Testdata={

			   Name : "Rajan",
			   Age : 30,
			   Desination : "Lead"
		   } 

		   let newTestdata:ITest =Testdata;
 ```
   ### Class 
    Access Modifier used in typescript 
         * Public (By Default)
         * Private
         * Protected
		 
   Class with Public and private member 
```TypeScript
	   class Test 
	    {
			Name:string; //Public 
			private Age:number; //private 
			#Salary:string; //ECMA Script
		 }	
```
### Class with static member 
```TypeScript
	   class Test 
	    {
			static Name:string; ="Rajan"
			static Age:number; //private 
			
		 }	

// when call static member not required this 

		    	console.log (Test.Name)	   
   ```
### Class with constructor 
```TypeScript
		 class Test 
		 {
			 constructor()
			  {

			  }
		 } 
  
		  Constructor  Parameter normal way accees 

		 class Test 
		 {
			 name:string;

			 constructor(Name:string)
			  {
				  this.name=Name;
			  }
			  console.log(this.name);
		 } 

  Another easier way

	 class Test 
		 {
			 constructor(public Name:string)
			  {
				  
			  }
			   console.log(this.Name);
		 } 
 ```
## Type Script Modules
    
	       Why do we need  Modules ?
		      
			   1. Encapsalation 2. Reuseablity  3. Create Higher level abstrations

### Export Key word

         By use of this functionality we can expose your class,function or interface in another module
```TypeScript
		   export interface IPerson {}
		      export function GetPersonName() {}
			     export default Class Person {}
				    Class Person1 {} // did not access other module


		     Another way declare export class 

                     interface IPerson {}
		       function GetPersonName() {}
			      default Class Person {}
				  
					export {IPerson,GetPersonNam as Getname,Person }
](url)](url)
