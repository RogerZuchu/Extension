# Extension

# extension navDirection
```
extension UIViewController{
    static func createInstantiate(nameStoryboard:String,withIdentifier:String)->UIViewController{
        let storyboard = UIStoryboard(name: nameStoryboard, bundle: nil)
        let gotoNextStoryboard = storyboard.instantiateViewController(withIdentifier: withIdentifier) as! UIViewController
        return gotoNextStoryboard
    }
    
}

```


# extension  bar

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

result là chuỗi sau khi cắt

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


# extension check internet Alamofire

```
import Alamofire

public class InternetConnectionManager {
    static var shared = InternetConnectionManager()
    private init() {
    }
    func isConnectedToInternet() ->Bool {
        return NetworkReachabilityManager()!.isReachable
    } 
}
```


# extension lưu hình ảnh vào cache để load khi offline
```
extension UIImageView {
  func loadUrl(_ url: String?) {
        ImageCache.shared.costLimit = 1024 * 1024 * 100 // 100 MB
        ImageCache.shared.countLimit = 100
        ImageCache.shared.ttl = 120 // Invalidate image after 120 sec
        var url1 = URL(string: url!)
        // Read and write images
        let request = ImageRequest(url: url1!)
        let image = ImageCache.shared[request]
        Nuke.loadImage(with: URL(string: url!)!, into: self)
    }
}
```

    

                    
                   
