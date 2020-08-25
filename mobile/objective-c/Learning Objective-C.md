## **Variables and Constants**

To create a public attribute, we must create it in the .h class:
```objective-c
@interface ViewCOntroller : UIViewControoler{
  //Public attribute for access
  NSString * word;
}
```

```objective-c
@implementation ViewCOntroller
- (void)viewDidLoad{
    [super viewDidLoad];

    //Public attribute of the ViewController class, created in the class .h
    word = @"Hello";

    //Internal attributes of the changeable .m classes
    NSString *word2;
    word2 = @"Hello to word 2";
    word2 = @"Goodbye init word 2";

    //Creating constant within the .m class
    NSString * const word3 = @"Xurupita";
    word3 = @"Trocando xurupita"; //It will not work
}
```


## **Strings**

## **Integers**

## **Floats & Doubles - Decial 32 e 64 biy**

## **Booleans**

## **Arrays**

## **If Statements**

## **AND and OR Statements**

## **For Loops**

## **While Loops**
```objective-c
  int cont = 0;
  while(condition){}
```
  Exemple:
  
```objective-c
  int cont = 0;
  while(cont < 10){
    number += 1;
    NSLog(@"%i", number);
  }
```

## **Switch Statements**

  ```objective-c
  int number = 1;
  switch(number){
    case 1:
      NSLog(@"Number 1");
      break;
      
    case 2:
      NSLog(@"Number 2");
      break;
      
    case 3:
      NSLog(@"Number 3");
      break;
      
    default:
      NSLog(@"Not Availble");
      break;
  }
  ```

## **Functions**


Create the function inner the class
```objective-c
- (void)trigger {
    self.label.text = @"I got triggered";
}
```

Call the function within the other function
```objective-c
- (IBAction)button:(id)sender{
    [self trigger];
}
```
