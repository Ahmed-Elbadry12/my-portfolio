import { test, expect } from '@playwright/test';

test('valid login', async ({ page }) =>{
 //enter to website
 await page.goto('https://practice.expandtesting.com/login');
 //enter username
  await page.locator("//input[@id='username']").fill('practice');
  //enter password 
  await page.locator("//input[@id='password']").fill("SuperSecretPassword!");
  //click on login button
  await page.locator("//button[normalize-space()='Login']").click();
  //expected result 
  await expect(page.locator("div[id='flash'] b")).toContainText("You logged into a secure area!");
  
  });
  
