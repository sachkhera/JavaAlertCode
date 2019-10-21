	//package intr;
	
	
	
	import org.openqa.selenium.By;
  import org.openqa.selenium.WebDriver;
  import org.openqa.selenium.chrome.ChromeDriver;
	import org.openqa.selenium.chrome.ChromeDriverService;
	import org.testng.Assert;
	import org.testng.annotations.Test;
	
	public class javaScriptAlert {
	
	String actual = "You clicked: Ok";
	@Test
	public void clickjAlert() {
	
	System.setProperty(ChromeDriverService.CHROME_DRIVER_EXE_PROPERTY,"//Users//sachinkhera//Downloads//chromedriver" );
	      WebDriver driver  = new ChromeDriver();
	        driver.get("https://the-internet.herokuapp.com");
	        driver.findElement(By.xpath("//a[contains(text(),'JavaScript Alerts')]")).click();
	        driver.findElement(By.xpath("//button[contains(text(),'Click for JS Confirm')]")).click();
	        String text = driver.switchTo().alert().getText();
	          System.out.println(text);
	          driver.switchTo().alert().accept();
	        String result = driver.findElement(By.xpath("//p[@id='result']")).getText();
	          System.out.println(result);
	          Assert.assertEquals(actual, result);
	
	}
	
	}


