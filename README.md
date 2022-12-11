start.spring.io

welcome page
templete engine


main > java > hello.hellospring > controller 패키지 생성 > HelloControler.java 생성

HelloController.java 
==>
package hello.hellospring.controller;

import org.springframework.ui.Model;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class HelloController {

    @GetMapping("hello")
    public String hello(Model model) {
        model.addAttribute("data", "hello!!");
        return "hello";
    }
}
실제 값.
resources > index.html localhost:8080 메인 페이지?
==>
<!DOCTYPE HTML>
<html>
<head>
    <title>Hello</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
</head>
<body>
Hello
<a href="/hello">hello</a>
</body>
</html>

resources > templates > hello.html localhost:8080/hello 서브 페이지??

===================================================================
Terminal에서 실행 시키기	ctrl - C 서버 닫기
cd hello-spring > ./gradlew build > cd build > cd libs >
> java -jar hello-spring-0.0.1-SNAPSHOT.jar 
