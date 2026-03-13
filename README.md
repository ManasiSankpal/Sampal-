FacultativeAmount: {
  selector: "//div[@row-index='0']//div[@col-id='amount']",
  locateStrategy: "xpath"
}

AmountInput: {
  selector: "//div[contains(@class,'ag-cell-inline-editing')]//input",
  locateStrategy: "xpath"
}


browser
.waitForElementVisible(this.elements.FacultativeAmount, 5000)

.click(this.elements.FacultativeAmount)

.keys(browser.Keys.ENTER)   // start edit mode

.waitForElementVisible(this.elements.AmountInput, 5000)

.clearValue(this.elements.AmountInput)

.setValue(this.elements.AmountInput, text['Fac Amount'])

.keys(browser.Keys.ENTER)

.pause(2000);
