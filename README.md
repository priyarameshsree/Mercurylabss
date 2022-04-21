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
    //address
		@Test
		public void c_address() {
		driver.findElement(By.name("address1")).sendKeys("Chennai");
		driver.findElement(By.xpath("//b[text()='City:']/following::input[1]")).sendKeys("Chennai");
		driver.findElement(By.name("state")).sendKeys("TamilNadu");
		driver.findElement(By.name("postalCode")).sendKeys("600028");
		Select drpdown=new Select (driver.findElement(By.name("country")));
		drpdown.selectByVisibleText("GERMANY");
		}
		//userinforamtion
		@Test
		public void e_userInformation() {
		driver.findElement(By.id("email")).sendKeys("priya@gmail.com");
		driver.findElement(By.name("password")).sendKeys("123456789");
		driver.findElement(By.name("confirmPassword")).sendKeys("123456789");
		driver.findElement(By.name("submit")).click();
	}

}

