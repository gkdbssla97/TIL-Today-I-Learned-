# Singleton pattern

싱글톤 패턴은 static을 응용하여 프로그램 전반에서 사용하는 인스턴스를 하나만 구현하는 방식이다.

싱글톤 패턴에서는 생성자를 반드시 명시적으로 만들고 그 접근 제어자를 private로 지정해야한다. 

> public class Company {   
    private static Company instance = new Company();  
    private Company() {}  
    public static Company getInstance() {  
        if(instance == null) {  
            instance = new Company();  
        }  
        return instance;
    }  
}

> public class CompanyTest {    
    public static void main(String[] args) {    
        Company com1 = Company.getInstance();   
        Company com2 = Company.getInstance();   
        System.out.println(com1 == com2);   
    }   
}   

com1과 com2를 비교하면 같은 참조 값을 가지는 동일한 인스턴스임을 알 수 있다. Company 클래스는 내부에 생성된 유일한 인스턴스 외에는 더 이상 인스턴스를 생성할 수 없다.
이와 같이 static을 사용하여 유일한 객체를 생성하는 싱글톤 패턴을 구현할 수 있다.