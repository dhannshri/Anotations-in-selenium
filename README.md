# Anotations-in-selenium
 Anotations in selenium  After test Before test After Method Before Method
 package ui;

import org.testng.annotations.AfterMethod;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import common.CommonDataSetup;
//BEFORETEST AFTERTEST BEFOREMETHOD AFTERMETHOD
public class LoginTest extends CommonDataSetup{
	
	@BeforeTest
	public void loginToApplication()
	{
		System.out.println("Login to Application");
	}
	
	@AfterTest
	public void logoutFromApplication() {
		System.out.println("Logout From Application");
	}
	@BeforeMethod
	public void connectToDB() {
		System.out.println("DB connected");
	}
	@AfterMethod
	public void disconnectedFromDB() {
		System.out.println("Disconnect DB connected");
	}
	
	@Test(priority=1, description="This is a login Test")
	public void aTest1() {
		System.out.println("Test1");
		}
	
	@Test(priority=2, description="This is a logout Test")
	public void bTest2() {
		System.out.println("Test2");
	}
	
}



