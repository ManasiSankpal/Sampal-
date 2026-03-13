const amountCell = "//div[@row-index='0']//div[@col-id='amount']";
const amountInput = "//input[contains(@class,'ag-input-field-input')]";

browser
.execute(function(xpath){
  const el = document.evaluate(xpath, document, null, XPathResult.FIRST_ORDERED_NODE_TYPE, null).singleNodeValue;
  if(el){ el.scrollIntoView({block:'center', inline:'center'}); }
}, [amountCell])

.waitForElementVisible({selector: amountCell, locateStrategy:'xpath'},10000)

.click({selector: amountCell, locateStrategy:'xpath'})

.waitForElementVisible({selector: amountInput, locateStrategy:'xpath'},5000)

.clearValue({selector: amountInput, locateStrategy:'xpath'})

.setValue({selector: amountInput, locateStrategy:'xpath'}, text['Fac Amount'])

.keys(browser.Keys.ENTER);
