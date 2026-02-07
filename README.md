# Sampal-

ADDMainSearchGroup(data) {
  const browser = this.api;

  const resultRowXpath = `//div[@role='row']//div[text()='${data['Company Code']}']`;

  browser
    .usexpath()
    .pause(2000)

    // Select field: Company code
    .click(this.elements.searchField.selector)
    .click(`//span[text()='Company code']`)

    // Select operator: contains
    .click(this.elements.operatorDropdown.selector)
    .click(`//span[text()='contains']`)

    // Enter filter value
    .clearValue(this.elements.filterInput.selector)
    .setValue(this.elements.filterInput.selector, data['Company Code'])

    // Apply / wait
    .pause(2000)

    // ASSERTION – THIS IS THE REAL TEST
    .waitForElementVisible(
      resultRowXpath,
      5000,
      `Company code ${data['Company Code']} is present in search results`
    )

    // Optional strong assertion
    .assert.elementPresent(
      resultRowXpath,
      `Search result verified for company code ${data['Company Code']}`
    );

  return this;
}
