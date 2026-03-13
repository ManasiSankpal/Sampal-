const amountCell = "//div[@row-index='0']//div[@col-id='amount']";
const amountInput = "//input[contains(@class,'ag-input-field-input')]";

browser
.waitForElementVisible({selector: amountCell, locateStrategy: "xpath"}, 10000)

.moveToElement({selector: amountCell, locateStrategy: "xpath"}, 5, 5)

.doubleClick({selector: amountCell, locateStrategy: "xpath"})   // start edit mode

.waitForElementVisible({selector: amountInput, locateStrategy: "xpath"}, 5000)

.clearValue({selector: amountInput, locateStrategy: "xpath"})

.setValue({selector: amountInput, locateStrategy: "xpath"}, text['Fac Amount'])

.keys(browser.Keys.ENTER);
