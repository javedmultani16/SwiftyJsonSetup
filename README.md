# SwiftyJsonSetup
<img width="77" alt="Screenshot 2019-09-26 at 4 40 35 PM" src="https://user-images.githubusercontent.com/16849127/65672896-636a7b00-e07c-11e9-871e-9c30b5b1d5b2.png">

Download "SwiftyJSONAccelerator" it makes more easy to parse json just paste your json response and it will give you ready class, you have to just drag and drop taht class in your project and ready to use.

<img width="751" alt="Screenshot 2019-09-26 at 5 27 07 PM" src="https://user-images.githubusercontent.com/16849127/65676691-e8f12980-e082-11e9-8384-f6c9532134a1.png">


We have to use this library:
https://github.com/SwiftyJSON/SwiftyJSON

- Install the intructed Pod using pod installation.
- Import framework like...
``` 
import SwiftyJSON
```
- Parse your json response like...

```
         let arrayStudentMain = dataDic["Student"] as! [NSArray]
            let swiftArray = arrayStudentMain as AnyObject as! [Any]
            for i in 0..<swiftArray.count {
                let json = JSON(swiftArray[i])
                let objStudent : ObjStudent = ObjStudent.init(json: json)
                self.studentMainArray.append(objStudent)
            }
