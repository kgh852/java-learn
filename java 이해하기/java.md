# class

```java
class person {
    int age = 17;
    String name = "김구현";
    String school = "경소고";
}

public class Main {
    public static void main(String[] args) {
        person guhyun = new person();
        System.out.println(guhyun.age);
        System.out.println(guhyun.name);
        System.out.println(guhyun.school);
    }
}
```
person class 정의 ->
person class 인스턴스를 바탕으로 guhyun 객체 생성 ->
guhyun 객체에서 속성에 접근하여 출력

# Method
```java
public class Main {
    static void myMethod() {
        System.out.println("김구현");
    }

    public static void main(String[] args) {
        myMethod();
    }
}

```
myMethod 생성 ->
myMethod 값 출력

# Inheritance

```java
class Person {
    int age;
    String name;

    public Person(int age, String name) {
        this.age = age;
        this.name = name;
    }
}

class Student extends Person {
    String school;

    public Student(int age, String name, String school) {
        super(age, name);
        this.school = school;
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student(17, "김구현", "경소고");
        System.out.println(student.age);
        System.out.println(student.name);
        System.out.println(student.school);
    }
}
```
person class 정의 ->
student class 정의(student class는 person class를 상속 받는다) ->
Student class 인스턴스를 바탕으로 student객체 생성 ->
student 객체에서 속성에 접근하여 출력

# Interface

```java
interface Person {
    int getAge();
    String getName();
}

class Student implements Person {
    private int age;
    private String name;
    private String school;

    public Student(int age, String name, String school) {
        this.age = age;
        this.name = name;
        this.school = school;
    }
    public int getAge() {
        return age;
    }
    public String getName() {
        return name;
    }
    public String getSchool() {
        return school;
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student(17, "김구현", "경소고");
        System.out.println(student.getAge());
        System.out.println(student.getName());
        System.out.println(student.getSchool());
    }
}
```
Person 인터페이스 정의 ->
Student 클래스가 Person 인터페이스를 구현 ->
Main 클래스에서 stuent 객체 생성 및 출력 

# Encapsulation
```java
class Person {
    private String name;

    public String getName() {
        return name;
    }

    public void setName(String newName) {
        this.name = newName;
    }
}

public class Main {
    public static void main(String[] args) {
        Person myObj = new Person();
        myObj.setName("김구현");
        System.out.println(myObj.getName());
    }
}
```
Person 클래스 정의 ->


