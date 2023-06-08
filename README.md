### Câu 1: khái niệm lập trình hướng đối tượng là gì ?

> Lập trình hướng đối tượng (OOP) là phương pháp lập trình trong đó chương trình được xây dựng xung quanh các đối tượng. Đối tượng có thuộc tính và phương thức tương ứng, và tương tác thông qua việc gửi nhận thông điệp. OOP giúp tái sử dụng mã, tăng tính bảo mật và dễ bảo trì, và cung cấp cách tổ chức mã nguồn dễ hiểu và quản lý hơn.

### Câu 2: Nêu cú pháp cách khai báo tên lớp và lấy ví dụ ?
***Cú pháp :***

```
public class TenLop {
    // Các thành phần của lớp
}
```
***Trong đó :***
* `public`: Một từ khóa chỉ định mức độ truy cập của lớp. public cho phép lớp được truy cập từ bất kỳ đâu trong chương trình.
* `class`: Từ khóa để khai báo một lớp trong Java.
* `TenLop`: Tên của lớp được đặt theo quy tắc đặt tên trong Java, ví dụ như CamelCase (chữ cái đầu tiên viết thường, các chữ cái đầu tiên của các từ tiếp theo viết hoa).

***Ví dụ :***
```
public class HinhTron {
    // Các thuộc tính và phương thức của lớp HinhTron
}
```
> Trong ví dụ trên, chúng ta khai báo một lớp có tên là HinhTron, đại diện cho một hình tròn. Lớp này có thể chứa các thuộc tính như bán kính, phương thức để tính diện tích, chu vi, và các hành vi khác liên quan đến hình tròn.

### Câu 3: Nêu cú pháp cách khai báo phương thức? Có mấy loại khai báo phương thức và lấy ví dụ từng loại khai báo phương thức.
***Cú pháp :***

![markdown](https://imgur.com/3FVbMqU.png)

**Có 3 loại khai báo phương thức**
1. Phương thức không trả về giá trị và không có tham số:
```
public void printHello() {
    System.out.println("Hello!");
}
```

2. Phương thức có giá trị trả về và không có tham số:
```
public int calculateSum() {
    int a = 5;
    int b = 10;
    int sum = a + b;
    return sum;
}
```

3. Phương thức có giá trị trả về và có tham số:
```
public int calculateProduct(int a, int b) {
    return a * b;
}
```

### Câu 4: Định nghĩa lớp và đối tượng? Lấy ví dụ minh hoạ về lớp và đối tượng? Cách phân biệt giữa lớp và đối tượng?
> Lớp là một mô hình, còn đối tượng là một thực thể cụ thể của lớp.

***Ví dụ về lớp :***
```
public class Circle {
    // Thuộc tính
    private double radius;

    // Phương thức
    public double getRadius() {
        return radius;
    }

    public void setRadius(double radius) {
        this.radius = radius;
    }

    public double calculateArea() {
        return Math.PI * radius * radius;
    }
}
```

***Ví dụ về đối tượng :***
```
public class Main {
    public static void main(String[] args) {
        Circle circle1 = new Circle();  // Tạo một đối tượng circle1 từ lớp Circle
        circle1.setRadius(5.0);  // Gán giá trị cho thuộc tính radius của đối tượng circle1
        double area = circle1.calculateArea();  // Gọi phương thức calculateArea() của đối tượng circle1
        System.out.println("Area of circle1: " + area);
    }
}
```
![Imgur](https://imgur.com/OEtmrEM.png)

### Câu 5: Hàm khởi tạo là gì? Nêu đặc điểm của hàm khởi tạo? Có mấy loại hàm khởi tạo lấy ví dụ minh hoạ
> Hàm khởi tạo (constructor) là một phương thức đặc biệt trong một lớp được sử dụng để khởi tạo đối tượng. Nó có tên giống với tên của lớp và được gọi tự động khi một đối tượng mới được tạo.

***Đặc điểm của hàm khởi tạo:***
1. Tên hàm khởi tạo phải giống với tên của lớp.
2. Hàm khởi tạo không có kiểu trả về (void, int, String, ...).
3. Hàm khởi tạo có thể có tham số hoặc không có tham số.

**Có 2 loại hàm khởi tạo**
1. Hàm khởi tạo không có tham số: Được sử dụng để khởi tạo đối tượng mà không cần truyền bất kỳ tham số nào.

**Ví dụ:**
```
public class Person {
    private String name;
    private int age;

    // Hàm khởi tạo không có tham số
    public Person() {
        name = "John Doe";
        age = 0;
    }

    // ...
}
```

2. Hàm khởi tạo có tham số: Được sử dụng để khởi tạo đối tượng và truyền giá trị cho các thuộc tính của đối tượng.

**Ví dụ:**
```
public class Car {
    private String brand;
    private String model;
    private int year;

    // Hàm khởi tạo có tham số
    public Car(String brand, String model, int year) {
        this.brand = brand;
        this.model = model;
        this.year = year;
    }

    // ...
}
```

### Câu 6: Hàm truy vấn là gì? Hàm truy cập là gì? Nêu ví dụ minh hoạ
> Hàm truy vấn (getter) là một phương thức trong lớp được sử dụng để truy xuất và trả về giá trị của một thuộc tính (biến thành viên) trong đối tượng.

**Ví dụ:**
```
public class Person {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // Hàm truy vấn getName trả về giá trị của thuộc tính name
    public String getName() {
        return name;
    }

    // Hàm truy vấn getAge trả về giá trị của thuộc tính age
    public int getAge() {
        return age;
    }

    // ...
}
```

> Hàm truy cập (setter) là một phương thức trong lớp được sử dụng để thiết lập (đặt) giá trị cho một thuộc tính trong đối tượng.

**Ví dụ:**
```
public class Car {
    private String brand;
    private String model;

    public Car(String brand, String model) {
        this.brand = brand;
        this.model = model;
    }

    // Hàm truy cập setBrand thiết lập giá trị cho thuộc tính brand
    public void setBrand(String brand) {
        this.brand = brand;
    }

    // Hàm truy cập setModel thiết lập giá trị cho thuộc tính model
    public void setModel(String model) {
        this.model = model;
    }

    // ...
}
```

### Câu 7: Thế nào là kế thừa?
> Kế thừa là quá trình một lớp con lấy các thuộc tính và phương thức của một lớp cha để sử dụng và mở rộng chúng. Nó cho phép lớp con kế thừa và mở rộng các tính năng của lớp cha, giúp tăng tính tái sử dụng và mở rộng trong lập trình hướng đối tượng.

### Câu 8: Có mấy dạng kế thừa lấy ví dụ minh hoạ
> Trong lập trình hướng đối tượng, có ba dạng kế thừa chính: kế thừa đơn, kế thừa đa cấp và kế thừa đa hình. Dưới đây là ví dụ minh hoạ cho mỗi dạng kế thừa:

1. Kế thừa đơn (Single inheritance):

```
class Animal {
    protected String name;

    public void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    public void bark() {
        System.out.println("Dog is barking");
    }
}
```

2. Kế thừa đa cấp (Multilevel inheritance):

```
class Animal {
    protected String name;

    public void eat() {
        System.out.println("Animal is eating");
    }
}

class Mammal extends Animal {
    public void run() {
        System.out.println("Mammal is running");
    }
}

class Dog extends Mammal {
    public void bark() {
        System.out.println("Dog is barking");
    }
}
```

3. Kế thừa đa hình (Hierarchical inheritance):

```
class Animal {
    protected String name;

    public void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    public void bark() {
        System.out.println("Dog is barking");
    }
}

class Cat extends Animal {
    public void meow() {
        System.out.println("Cat is meowing");
    }
}
```

### Câu 9: Overriding là gì?
> Overriding là quá trình định nghĩa lại một phương thức trong lớp con có cùng tên, cùng số lượng tham số và cùng kiểu trả về với phương thức đã có trong lớp cha. Phương thức của lớp con sẽ được thực thi thay vì phương thức của lớp cha khi gọi phương thức đó.

### câu 10: So sánh Overriding và Overloading
`Overriding`
> Overriding là quá trình định nghĩa lại phương thức trong lớp con từ lớp cha có cùng tên, cùng số lượng tham số và cùng kiểu trả về.

`Overloading`
> Overloading là quá trình định nghĩa nhiều phương thức cùng tên nhưng có các tham số khác nhau trong cùng một lớp. Các phương thức Overloading phải có tên giống nhau nhưng khác nhau về số lượng tham số, kiểu dữ liệu của các tham số hoặc cả hai.
