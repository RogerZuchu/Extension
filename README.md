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
import Nuke
extension UIImageView {
    func loadUrl(_ url: String?) {
        Nuke.loadImage(with: URL(string: url!)!, into: self)
    }
}
```
