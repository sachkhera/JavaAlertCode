3.	//package intr;
4.	
5.	
6.	
7.	import org.openqa.selenium.By;
8.	import org.openqa.selenium.WebDriver;
9.	import org.openqa.selenium.chrome.ChromeDriver;
10.	import org.openqa.selenium.chrome.ChromeDriverService;
11.	import org.testng.Assert;
12.	import org.testng.annotations.Test;
13.	
14.	public class javaScriptAlert {
15.	
16.	String actual = "You clicked: Ok";
17.	@Test
18.	public void clickjAlert() {
19.	
20.	System.setProperty(ChromeDriverService.CHROME_DRIVER_EXE_PROPERTY,"//Users//sachinkhera//Downloads//chromedriver" );
21.	      WebDriver driver  = new ChromeDriver();
22.	        driver.get("https://the-internet.herokuapp.com");
23.	        driver.findElement(By.xpath("//a[contains(text(),'JavaScript Alerts')]")).click();
24.	        driver.findElement(By.xpath("//button[contains(text(),'Click for JS Confirm')]")).click();
25.	        String text = driver.switchTo().alert().getText();
26.	          System.out.println(text);
27.	          driver.switchTo().alert().accept();
28.	        String result = driver.findElement(By.xpath("//p[@id='result']")).getText();
29.	          System.out.println(result);
30.	          Assert.assertEquals(actual, result);
31.	         
32.	         
33.	         
34.	
35.	}
36.	
37.	}


