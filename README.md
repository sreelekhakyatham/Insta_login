package Webdriver;

import java.time.Duration;


import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class Insta_login {

	public static void main(String[] args) throws Exception {
		WebDriver driver=new ChromeDriver();
		driver.get("https://www.instagram.com/accounts/login/");
		driver.manage().window().maximize();
		driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(30));
				
		driver.findElement(By.xpath("//*[@id=\"loginForm\"]/div/div[1]/div/label/input")).sendKeys("9848452174");
		Thread.sleep(3000);
		driver.findElement(By.xpath("//input[contains(@aria-label,'Password')]")).sendKeys("123456789");
		Thread.sleep(3000);
		driver.findElement(By.xpath("(//div[contains(.,'Log in')])[14]")).click();
		driver.close();
		
	}

}
