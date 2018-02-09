# Instance member cannot be used on type

简书

[https://www.jianshu.com/p/15d0e127957a](https://www.jianshu.com/p/15d0e127957a)

Stackoverflow

[https://stackoverflow.com/questions/32351343/instance-member-cannot-be-used-on-type](https://stackoverflow.com/questions/32351343/instance-member-cannot-be-used-on-type)

[https://stackoverflow.com/questions/32693150/whats-wrong-here-instance-member-cannot-be-used-on-type](https://stackoverflow.com/questions/32693150/whats-wrong-here-instance-member-cannot-be-used-on-type)



问题遇到的解决方式：

```swift
override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell = tableView.dequeueReusableCell(withIdentifier: "ExampleTableViewCell", for: indexPath) as! WillLearnTableViewCell
        
        //之前漏掉了这一行，添加即可
        let ExampleList = ExampleArray[indexPath.row]
        
        cell.Title.text = ExampleList.TitleLabel
        cell.Description.text = ExampleList.DesLabel
        cell.Notes.text = ExampleList.NotesLabel·
```


