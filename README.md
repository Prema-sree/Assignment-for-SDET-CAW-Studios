# Assignment-for-SDET-CAW-Studios
//Automation script for dynamic HTML table tag
package com.excel.utility;

 

import java.io.IOException;

import java.util.NoSuchElementException;

 

import org.openqa.selenium.By;

import org.openqa.selenium.WebDriver;

import org.openqa.selenium.WebElement;

import org.openqa.selenium.chrome.ChromeDriver;

import org.openqa.selenium.support.ui.Select;

 

import com.excel.lib.util.Xls_Reader;

 

public class DataDrivenExample {

 

              public static void main(String[] args) throws InterruptedException, IOException {

                            

//Webdriver code          

              System.setProperty("webdriver.chrome.driver","C:\\Users\\premasree.ramak\\eclipse-workspace\\SeleniumSample\\chromedriver.exe");

                             WebDriver driver=new ChromeDriver();

                             driver.get("https://testpages.herokuapp.com/styled/tag/dynamic-table.html");

                             // Find and click the "Table Data" button

        WebElement tableDataButton = driver.findElement(By.id("tableDataButtonId")); // Replace with the actual ID

        tableDataButton.click();

       

        // Find the input text box and input the JSON data

        WebElement inputTextBox = driver.findElement(By.id("tablehere")); // Replace with the actual ID

        inputTextBox.sendKeys("[{\"name\" : \"Bob\", \"age\" : 20, \"gender\": \"male\"}, {" +

                            "\"name\": \"George\", \"age\" : 42, \"gender\": \"male\"}, {" +

                            "\"name\": \"Sara\", \"age\" : 42, \"gender\": \"female\"}, {" +

                            "\"name\": \"Conor\", \"age\" : 40, \"gender\": \"male\"}, {" +

                            "\"name\": \"Jennifer\", \"age\" : 42, \"gender\": \"female\"}]");

       

        // Find and click the "Refresh Table" button

        WebElement refreshTableButton = driver.findElement(By.id("refreshtable")); // Replace with the actual ID

        refreshTableButton.click();

       

        // Close the WebDriver

  //      driver.quit();

 

 

              }

}
