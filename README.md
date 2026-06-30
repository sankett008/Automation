# Automation
Automation Project
package Seleniumrevision;

import java.util.List;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class handledropdowns {
	
	public static void main(String[] args) throws InterruptedException {
		WebDriver driver=new ChromeDriver();
		driver.manage().window().maximize();
		
		driver.get("https://testautomationpractice.blogspot.com/");
		
	WebElement	drp=driver.findElement(By.xpath("//select[@id='country']"));
	 Select s=new Select(drp);
	  // s.selectByValue("germany");
	// s.selectByIndex(3);
	 
	    List<WebElement>coun=s.getOptions();
	    System.out.println(coun.size());
	    
	    for(WebElement op:coun) {
	    	System.out.println(op.getText());
	    }
		
