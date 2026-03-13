browser
.waitForElementVisible("//div[@row-index='0']//div[@col-id='amount']",5000)
.click("//div[@row-index='0']//div[@col-id='amount']")
.keys(browser.Keys.ENTER)
.pause(500)
.keys(text['Fac Amount'])
.keys(browser.Keys.ENTER);
