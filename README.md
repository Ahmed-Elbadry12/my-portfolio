import { test, expect } from '@playwright/test';

test(' login page', async ({ page }) =>{
 
await page.goto('https://practice.expandtesting.com/login');

await expect(
  page.getByAltText("Best Website for Practice Automation Testing: Free UI and REST API Examples and Apps. Using Cypress, Playwright, Selenium, WebdriverIO and Postman.")).toBeVisible();
  
  await expect (page.getByText("SuperSecretPassword!")).toBeVisible();
  


});


