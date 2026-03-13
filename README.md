browser
.waitForElementVisible("//div[@col-id='amount']",5000)
.click("//div[@col-id='amount']")
.waitForElementVisible("//input[contains(@class,'ag-input-field-input')]",5000)
.clearValue("//input[contains(@class,'ag-input-field-input')]")
.setValue("//input[contains(@class,'ag-input-field-input')]", text['Fac Amount'])
.keys(browser.Keys.ENTER);
