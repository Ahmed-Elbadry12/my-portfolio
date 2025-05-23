import { test, expect } from '@playwright/test';

test('valid login', async ({ page }) =>{
  await page.goto('https://practice.expandtesting.com/login');
  await page.locator("//input[@id='username']").fill('practice');
  await page.locator("//input[@id='password']").fill("SuperSecretPassword!");
  await page.locator("//button[normalize-space()='Login']").click();
  await expect(page.locator("div[id='flash'] b")).toContainText("You logged into a secure area!");
  
  });
  
