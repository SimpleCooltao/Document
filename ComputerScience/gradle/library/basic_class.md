```
task helloJavaBean << {
    Person p = new Person()

    println "名字是：${p.name}"
    p.name = "张三"
    println "名字是：${p.name}"
    println "年龄是：${p.age}"
}

class Person {
    private String name

    public int getAge(){
        12
    }
}
```