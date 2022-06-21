# Extension

# extension navDirection
```
extension UIViewController{
    func directionToViewController(nameStoryboard:String,withIdentifier:String){
        let storyboard = UIStoryboard(name: nameStoryboard, bundle: nil)
        let gotoNextStoryboard = storyboard.instantiateViewController(withIdentifier: withIdentifier) as! UIViewController
        self.navigationController?.pushViewController(gotoNextStoryboard, animated: true)
    }  
}

```


# extension bar

```
extension UIViewController{
    func hideBarButton(){
        self.navigationItem.hidesBackButton = true
    }
}
```


# extension load Image From Internet

```
install pod 'Nuke', '~> 9.0'
import Nuke
extension UIImageView {
    func loadUrl(_ url: String?) {
        Nuke.loadImage(with: URL(string: url!)!, into: self)
    }
}
```


# extension cut String

offsetBy 0 là từ bên trái qua bên phải
offsetBy -16 là từ bên phải qua bên trái
result laf chuỗi sau khi cắt
string là 1 chuỗi nào đó
```
let string = self.user.created_at!
let start = string.index(string.startIndex,offsetBy: 0)
let end = string.index(string.endIndex,offsetBy: -16)
let result = string[start..<end]
self.lblCreateAt.text = "Since:  \(result)"
self.lblCreateAt.textColor = .white
```


# extension remove dấu phẩy trong số thập phân
```
func removeDecimal(result: Double) -> String {
            let value = String(format: "%g", result)
            return value
}
```



    

                    
                   
