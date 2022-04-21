# Mercurylabss
Working mercurylabs
package testNgFramework;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
import org.testng.annotations.Test;

public class Mercuryas {
	WebDriver driver;

		@Test
		public void a_pageLoad() {
		System.setProperty("webdriver.chrome.driver","E:\\selenium\\chrome\\chromedriver_win32\\chromedriver.exe");
		driver=new ChromeDriver();
		driver.get("https://demo.guru99.com/test/newtours/register.php");
		driver.manage().window().maximize();
		}
		//contact Information
		@Test
		public void b_contactInformtion() {
		driver.findElement(By.name("firstName")).sendKeys("Banupriya");
		driver.findElement(By.name("lastName")).sendKeys("Rameshbabu");
		driver.findElement(By.name("phone")).sendKeys("123456789");
		driver.findElement(By.id("userName")).sendKeys("hhhh@gmail.com");
		}
    }
