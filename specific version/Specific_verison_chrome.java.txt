public class Selenium_grid_SetMetadata {
	WebDriver driver;
	
	@Test
	public void test1() throws MalformedURLException {
		String browserversion="122.0.6261.69";
		ChromeOptions fos=new ChromeOptions();
		
    RemoteWebDriver driver = new RemoteWebDriver(new URL("http://172.19.16.1:4444"), fos);
    String actualbrowserversion=driver.getCapabilities().getBrowserVersion().toString();
    if(actualbrowserversion.equals(browserversion)) {
    driver.get("https://www.flipkart.com");
    }
    else {
    	System.out.println("Desired Chrome version " + browserversion + " not available. Actual version is: " + actualbrowserversion);
    }
}
}
