---

title: Constructer
date: 2021-05-25
name: 이현곤

---
# [ 생성자 개념 및 형태 ] 

> ` 생성자 = 객체가 생성될 때 자동으로 호출되는 메소드로써 객체의 초기화를 위해 실행된다. `

> ` 생성자는 2가지의 유형이 존재한다 `

1. public Rectangle2()  = 매개변수 없는 생성자 
2. public Rectangle2(int r, int n)  = 매개 변수를 가진 생성자

> ` 주의할 점 `
* 생성자의 이름은 클래스 이름과 동일하다.
* 생성자의 목적은 객체가 생성될 때, 필요한 초기 작업을 위함이다.
* 생성자에 리턴 타입을 지정할 수 없다. 리턴값이 없다고 해서, void를 리턴 타입으로 지정해도 안된다.
* 생성자는 new를 통해 객체를 생성할 때 한번만 호출된다.
* 생성자는 여러 개 작성(오버로딩) 할 수 있다.
  매개변수의 개수와 타입만 다르다면, 클래스 내의 생성자를 여러 개 둘 수 있다.
  - 예 ) public Rectangle()   &&   public Rectangle(int r, int n)
      
> ` 코드 예시 `

[Rectangle2 Class 메서드] 

```java
package Chapter5_constructer;
public class Rectangle2 {

	int width;
        int height;
	
       
	    public Rectangle2() { // 매개변수 없는 생성자
	        width = 1; // 필드 초기화
	    }
	 
	    public Rectangle2(int r, int n) { // 매개 변수를 가진 생성자
	        width = r; height = n; // 매개 변수로 필드 초기화
	    }
	    
	    public double getArea() { // 사각형의 면적 계산 메소드
	        return width * height;
	    }
	}
  ```
 [Rectangle2 Main 메서드] 
 
 ```java
 package Chapter5_constructer;
 public class RectangleTest2 {

	public static void main(String[] args) {
	
		
	 Rectangle2 rec = new Rectangle2(); // Rectangle 객체 생성
	 rec.height = 20; // 높이를 20으로 초기화
         double area = rec.getArea(); // 면적을 계산하여 area 
	System.out.println(area); // 면적 출력
		 
		 
	Rectangle2 Rrec = new Rectangle2(5, 10); // 객체 생성. r에 5를 n에 10을 넣어 초기화.
	double area1 = Rrec.getArea();
	System.out.println(area1);
	 
	    }
	

		  
	}
 ```		
