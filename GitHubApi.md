### GitHub Api Demo
![](https://img.shields.io/badge/platform-OSX-red.svg)

> 供GitHub 开发者使用的Api 示例工程

*  官方Library [octoKit](https://github.com/octokit/octokit.objc)

> Swift4 中 使用NSTableView  
 
* NSTableView 设置 ContentMode : Cell Based
* 实现数据源方法

```swift
extension ViewController : NSTableViewDataSource{
     /** 返回行数 */
    func numberOfRows(in tableView: NSTableView) -> Int {
        return 2
    }
    /** 返回每行的数据 */
    func tableView(_ tableView: NSTableView, objectValueFor tableColumn: NSTableColumn?, row: Int) -> Any? {
        
        return "text \(row)"
    }
    /** 用数据给cell 赋值*/
    func tableView(_ tableView: NSTableView, setObjectValue object: Any?, for tableColumn: NSTableColumn?, row: Int) {
       
        let cell = tableView .make(withIdentifier: "github", owner: self) as! NSTableCellView
        cell.textField?.stringValue = object as! String
        
       
    }
    
    
}
``` 

