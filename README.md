# ECommerceSearchTest



import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.AfterClass;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.Test;

public class ECommerceSearchTest {
    private WebDriver driver;

    @BeforeClass
    public void setUp() {
        System.setProperty("webdriver.chrome.driver", "C:\\Users\\svvibhu\\Downloads\\chrome-win64\\chrome.exe");
        driver = new ChromeDriver();
    }

    @Test
    public void testProductSearch() {
        driver.get("https://example.com"); // Replace with your website URL

        WebElement searchInput = driver.findElement(By.id("search-input"));

   
        searchInput.sendKeys("smartphone");

      
        searchInput.submit();

       
    }

    @AfterClass
    public void tearDown() {
        driver.quit();
    }
}
