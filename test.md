# Full payload

```
    {
              "pdf_upload_id": "cae41859-df23-4f9f-8d28-74d613e08211",
              "pdf_filename": "file.pdf",
              "sha1": "18e950a281def4a5e3840a0fdfae84f08b277424",
              "supplier_vat": "BE0010012675",
              "supplier_name": "Supplier SA",
              "supplier_address": "Supplier street 1",
              "supplier_city": "Antwerpen",
              "supplier_postal_code": "2000",
              "supplier_country": "BE",
              "bank_account_number": "BE03974000000103",
              "bank_account_bic": "CDBXBE33",
              "customer_vat": "BE0010022375",
              "customer_name": "Customer SA",
              "customer_address": "Customer street 1",
              "customer_city": "Liège",
              "customer_postal_code": "4000",
              "customer_country": "BE",
              "invoice_number": "15701023",
              "invoice_date": "2015-11-06",
              "invoice_type": "invoice",
              "invoice_currency": "EUR",
              "invoice_due_date": "2015-12-31",
              "invoice_description": "Description of the invoice",
              "invoice_amount": "299.60",
              "invoice_amount_vat_excluded": "260.00",
              "invoice_amount_vat": "39.60",
              "payable_amount": "100",
              "payment_reference": "501570102394",
              "payment_reference_is_structured": true,
              "lines": [
                  {
                      "code": "pr01",
                      "description": "First Product",
                      "gl_account": "700000",
                      "quantity": "1.00",
                      "unit_price": "100",
                      "amount_vat_excluded": "100",
                      "vat_percentage": "21.00",
                      "amount_vat": "21.00",
                      "tax_category": "03"
                  },
                  {
                      "code": "pr02",
                      "description": "Second Product",
                      "gl_account": "701000",
                      "quantity": "2.00",
                      "unit_price": "30",
                      "amount_vat_excluded": "60",
                      "vat_percentage": "21.00",
                      "amount_vat": "12.60",
                      "tax_category": "03"
                  },
                  {
                      "code": "pr03",
                      "description": "Third Product",
                      "gl_account": "701000",
                      "quantity": "1.00",
                      "unit_price": "100",
                      "amount_vat_excluded": "100",
                      "vat_percentage": "6.00",
                      "amount_vat": "6.00",
                      "tax_category": "01"
                  }
              ],
              "taxes": [
                  {
                      "vat_percentage": "21.00",
                      "amount_vat_excluded": "160",
                      "amount_vat": "33.60",
                      "tax_category": "03"
                  },
                  {
                      "vat_percentage": "6.00",
                      "amount_vat_excluded": "100",
                      "amount_vat": "6.00",
                      "tax_category": "01"
                  }
              ]
    }
```   

## Full ubl
    
```
    <?xml version="1.0" encoding="UTF-8"?>
        <Invoice xmlns="urn:oasis:names:specification:ubl:schema:xsd:Invoice-2" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:udt="urn:un:unece:uncefact:data:specification:UnqualifiedDataTypesSchemaModule:2" xmlns:qdt="urn:oasis:names:specification:ubl:schema:xsd:QualifiedDatatypes-2" xmlns:ccts="urn:un:unece:uncefact:documentation:2" xmlns:cbc="urn:oasis:names:specification:ubl:schema:xsd:CommonBasicComponents-2" xmlns:cac="urn:oasis:names:specification:ubl:schema:xsd:CommonAggregateComponents-2">
        <cbc:UBLVersionID>2.1</cbc:UBLVersionID>
        <cbc:CustomizationID>urn:www.cenbii.eu:transaction:biitrns010:ver2.0:extended:urn:www.peppol.eu:bis:peppol4a:ver2.0</cbc:CustomizationID>
        <cbc:ProfileID>urn:www.cenbii.eu:profile:bii04:ver2.0</cbc:ProfileID>
        <cbc:ID>15701023</cbc:ID>
        <cbc:IssueDate>2015-11-06</cbc:IssueDate>
        <cbc:InvoiceTypeCode listID="UNCL1001">380</cbc:InvoiceTypeCode>
        <cbc:Note>Description of the invoice</cbc:Note>
        <cbc:TaxPointDate>2015-11-06</cbc:TaxPointDate>
        <cbc:DocumentCurrencyCode listID="ISO4217">EUR</cbc:DocumentCurrencyCode>
        <cac:AdditionalDocumentReference>
            <cbc:ID>test.pdf</cbc:ID>
            <cbc:DocumentType>CommercialInvoice</cbc:DocumentType>
            <cac:Attachment>
                <cbc:EmbeddedDocumentBinaryObject mimeCode="application/pdf"></cbc:EmbeddedDocumentBinaryObject>
            </cac:Attachment>
        </cac:AdditionalDocumentReference>
        <cac:AccountingSupplierParty>
            <cac:Party>
                <cbc:EndpointID schemeID="BE:VAT">BE0010012675</cbc:EndpointID>
                <cac:PartyName>
                    <cbc:Name>Supplier SA</cbc:Name>
                </cac:PartyName>
                <cac:PostalAddress>
                    <cbc:StreetName>Supplier street 1</cbc:StreetName>
                    <cbc:CityName>Antwerpen</cbc:CityName>
                    <cbc:PostalZone>2000</cbc:PostalZone>
                    <cac:Country>
                        <cbc:IdentificationCode listID="ISO3166-1:Alpha2">BE</cbc:IdentificationCode>
                    </cac:Country>
                </cac:PostalAddress>
                <cac:PartyTaxScheme>
                    <cbc:CompanyID schemeID="BE:VAT">BE0010012675</cbc:CompanyID>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:PartyTaxScheme>
                <cac:PartyLegalEntity>
                    <cbc:CompanyID schemeID="BE:VAT">BE0010012675</cbc:CompanyID>
                </cac:PartyLegalEntity>
            </cac:Party>
        </cac:AccountingSupplierParty>
        <cac:AccountingCustomerParty>
            <cac:Party>
                <cbc:EndpointID schemeID="BE:VAT">BE0010022375</cbc:EndpointID>
                <cac:PartyName>
                    <cbc:Name>Customer SA</cbc:Name>
                </cac:PartyName>
                <cac:PostalAddress>
                    <cbc:StreetName>Customer street 1</cbc:StreetName>
                    <cbc:CityName>Liege</cbc:CityName>
                    <cbc:PostalZone>4000</cbc:PostalZone>
                    <cac:Country>
                        <cbc:IdentificationCode listID="ISO3166-1:Alpha2">BE</cbc:IdentificationCode>
                    </cac:Country>
                </cac:PostalAddress>
                <cac:PartyTaxScheme>
                    <cbc:CompanyID schemeID="BE:VAT">BE0010022375</cbc:CompanyID>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:PartyTaxScheme>
                <cac:PartyLegalEntity>
                    <cbc:CompanyID schemeID="BE:VAT">BE0010022375</cbc:CompanyID>
                </cac:PartyLegalEntity>
            </cac:Party>
        </cac:AccountingCustomerParty>
        <cac:PaymentMeans>
            <cbc:PaymentMeansCode listID="UNCL4461">1</cbc:PaymentMeansCode>
            <cbc:PaymentDueDate>2015-12-31</cbc:PaymentDueDate>
            <cbc:PaymentID>501570102394</cbc:PaymentID>
            <cac:PayeeFinancialAccount>
                <cbc:ID schemeID="IBAN">BE03974000000103</cbc:ID>
                <cbc:Name/>
                <cac:FinancialInstitutionBranch>
                    <cac:FinancialInstitution>
                        <cbc:ID schemeID="BIC">CDBXBE33</cbc:ID>
                    </cac:FinancialInstitution>
                </cac:FinancialInstitutionBranch>
            </cac:PayeeFinancialAccount>
        </cac:PaymentMeans>
        <cac:TaxTotal>
            <cbc:TaxAmount currencyID="EUR">39.60</cbc:TaxAmount>
            <cac:TaxSubtotal>
                <cbc:TaxableAmount currencyID="EUR">160.00</cbc:TaxableAmount>
                <cbc:TaxAmount currencyID="EUR">33.60</cbc:TaxAmount>
                <cac:TaxCategory>
                    <cbc:ID schemeID="UNCL5305">S</cbc:ID>
                    <cbc:Percent>21.0</cbc:Percent>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:TaxCategory>
            </cac:TaxSubtotal>
            <cac:TaxSubtotal>
                <cbc:TaxableAmount currencyID="EUR">100.00</cbc:TaxableAmount>
                <cbc:TaxAmount currencyID="EUR">6.00</cbc:TaxAmount>
                <cac:TaxCategory>
                    <cbc:ID schemeID="UNCL5305">AA</cbc:ID>
                    <cbc:Percent>6.0</cbc:Percent>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:TaxCategory>
            </cac:TaxSubtotal>
        </cac:TaxTotal>
        <cac:LegalMonetaryTotal>
            <cbc:LineExtensionAmount currencyID="EUR">260.00</cbc:LineExtensionAmount>
            <cbc:TaxExclusiveAmount currencyID="EUR">260.00</cbc:TaxExclusiveAmount>
            <cbc:TaxInclusiveAmount currencyID="EUR">299.60</cbc:TaxInclusiveAmount>
            <cbc:PayableRoundingAmount currencyID="EUR">-0.00</cbc:PayableRoundingAmount>
            <cbc:PayableAmount currencyID="EUR">100.00</cbc:PayableAmount>
        </cac:LegalMonetaryTotal>
        <cac:InvoiceLine>
            <cbc:ID>1</cbc:ID>
            <cbc:InvoicedQuantity unitCode="C62" unitCodeListID="UNECERec20">1.00</cbc:InvoicedQuantity>
            <cbc:LineExtensionAmount currencyID="EUR ">100.0</cbc:LineExtensionAmount>
            <cac:TaxTotal>
                <cbc:TaxAmount currencyID="EUR">21.00</cbc:TaxAmount>
            </cac:TaxTotal>
            <cbc:AccountingCostCode>700000</cbc:AccountingCostCode>
            <cac:Item>
                <cbc:Name>First Product</cbc:Name>
                <cac:SellersItemIdentification>
                    <cbc:ID>pr01</cbc:ID>
                </cac:SellersItemIdentification>
                <cac:ClassifiedTaxCategory>
                    <cbc:ID schemeID="UNCL5305">S</cbc:ID>
                    <cbc:Percent>21.0</cbc:Percent>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:ClassifiedTaxCategory>
            </cac:Item>
            <cac:Price>
                <cbc:PriceAmount currencyID="EUR">100.0</cbc:PriceAmount>
            </cac:Price>
        </cac:InvoiceLine>
        <cac:InvoiceLine>
            <cbc:ID>2</cbc:ID>
            <cbc:InvoicedQuantity unitCode="C62" unitCodeListID="UNECERec20">2.00</cbc:InvoicedQuantity>
            <cbc:LineExtensionAmount currencyID="EUR ">60.0</cbc:LineExtensionAmount>
            <cac:TaxTotal>
                <cbc:TaxAmount currencyID="EUR">12.60</cbc:TaxAmount>
            </cac:TaxTotal>
            <cbc:AccountingCostCode>701000</cbc:AccountingCostCode>
            <cac:Item>
                <cbc:Name>Second Product</cbc:Name>
                <cac:SellersItemIdentification>
                    <cbc:ID>pr02</cbc:ID>
                </cac:SellersItemIdentification>
                <cac:ClassifiedTaxCategory>
                    <cbc:ID schemeID="UNCL5305">S</cbc:ID>
                    <cbc:Percent>21.0</cbc:Percent>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:ClassifiedTaxCategory>
            </cac:Item>
            <cac:Price>
                <cbc:PriceAmount currencyID="EUR">30.0</cbc:PriceAmount>
            </cac:Price>
        </cac:InvoiceLine>
        <cac:InvoiceLine>
            <cbc:ID>3</cbc:ID>
            <cbc:InvoicedQuantity unitCode="C62" unitCodeListID="UNECERec20">1.00</cbc:InvoicedQuantity>
            <cbc:LineExtensionAmount currencyID="EUR ">100.0</cbc:LineExtensionAmount>
            <cac:TaxTotal>
                <cbc:TaxAmount currencyID="EUR">6.00</cbc:TaxAmount>
            </cac:TaxTotal>
            <cbc:AccountingCostCode>701000</cbc:AccountingCostCode>
            <cac:Item>
                <cbc:Name>Third Product</cbc:Name>
                <cac:SellersItemIdentification>
                    <cbc:ID>pr03</cbc:ID>
                </cac:SellersItemIdentification>
                <cac:ClassifiedTaxCategory>
                    <cbc:ID schemeID="UNCL5305">AA</cbc:ID>
                    <cbc:Percent>6.0</cbc:Percent>
                    <cac:TaxScheme>
                        <cbc:ID>VAT</cbc:ID>
                    </cac:TaxScheme>
                </cac:ClassifiedTaxCategory>
            </cac:Item>
            <cac:Price>
                <cbc:PriceAmount currencyID="EUR">100.0</cbc:PriceAmount>
            </cac:Price>
        </cac:InvoiceLine>
    </Invoice>
```



###HEADER

- ID => "invoice_number": "15701023"
- IssueDate => "invoice_date": "2015-11-06"
- InvoiceTypeCode => "invoice_type": "invoice" ; enumeration = ["invoice", "credit_note"] =>  [380, 381] where **listID="UNCL1001"** is a hardcoded attribute http://www.unece.org/trade/untdid/d08a/tred/tred1001.htm
- Note => "invoice_description": "Description of the invoice",
- TaxPointDate =>  "invoice_date": "2015-11-06"
- DocumentCurrencyCode => "invoice_currency": "EUR" => **listID="ISO4217"** is a hardcoded attribute https://fr.wikipedia.org/wiki/ISO_4217 http://www.iso.org/iso/home/standards/currency_codes.htm
- AdditionalDocumentReference\\ID =>  "pdf_filename": "file.pdf" 
- AdditionalDocumentReference\\DocumentType : **CommercialInvoice"** is a hardcoded.
- AdditionalDocumentReference\\Attachment\\EmbeddedDocumentBinaryObject : file content where **mimeCode="application/pdf"** is hardcoded

**Question** : is CommercialInvoice related to InvoiceTypeCode ?

```
<cbc:ID>15701023</cbc:ID>
<cbc:IssueDate>2015-11-06</cbc:IssueDate>
<cbc:InvoiceTypeCode listID="UNCL1001">380</cbc:InvoiceTypeCode>
<cbc:Note>Description of the invoice</cbc:Note>
<cbc:TaxPointDate>2015-11-06</cbc:TaxPointDate>
<cbc:DocumentCurrencyCode listID="ISO4217">EUR</cbc:DocumentCurrencyCode>
<cac:AdditionalDocumentReference>
    <cbc:ID>test.pdf</cbc:ID>
    <cbc:DocumentType>CommercialInvoice</cbc:DocumentType>
    <cac:Attachment>
        <cbc:EmbeddedDocumentBinaryObject mimeCode="application/pdf"></cbc:EmbeddedDocumentBinaryObject>
    </cac:Attachment>
</cac:AdditionalDocumentReference>
```
        

#### AccountingSupplierParty


- Party\\EndpointID => "supplier_vat": "BE0010012675",
- Party\\PartyName\\Name => "supplier_name": "Supplier SA",
- Party\\PostalAddress\\StreetName => "supplier_address": "Supplier street 1",
- Party\\PostalAddress\\CityName  => "supplier_city": "Antwerpen",
- Party\\PostalAddress\\PostalZone  => "supplier_postal_code": "2000",
- Party\\PostalAddress\\Country\\IdentificationCode => "supplier_country": "BE",
- Party\\PartyTaxScheme\\CompanyID : "supplier_vat"=> "BE0010012675",
- Party\\PartyTaxScheme\\TaxScheme\\ID => "VAT" 
- Party\\PartyLegalEntity\\CompanyID : "supplier_vat"=> "BE0010012675",

**schemeID="BE:VAT"** is a hardcoded attribute for:
 - Party\\EndpointID  
 - Party\\PartyTaxScheme\\CompanyID  
 - Party\\PartyLegalEntity\\CompanyID  
   

Minimum PayLoad : 

```
<cac:AccountingSupplierParty>
    <cac:Party>
        <cbc:EndpointID schemeID="BE:VAT">BE0010012675</cbc:EndpointID>
        <cac:PartyName>
            <cbc:Name>Supplier SA</cbc:Name>
        </cac:PartyName>
        <cac:PartyTaxScheme>
            <cbc:CompanyID schemeID="BE:VAT">BE0010012675</cbc:CompanyID>
            <cac:TaxScheme>
                <cbc:ID>VAT</cbc:ID>
            </cac:TaxScheme>
        </cac:PartyTaxScheme>
        <cac:PartyLegalEntity>
            <cbc:CompanyID schemeID="BE:VAT">BE0010012675</cbc:CompanyID>
        </cac:PartyLegalEntity>
    </cac:Party>
</cac:AccountingSupplierParty>
```

Only for supplier, the VAT is always set.


```
<cac:AccountingSupplierParty>
    <cac:Party>
        <cbc:EndpointID schemeID="BE:VAT">BE0010012675</cbc:EndpointID>
        <cac:PartyName>
            <cbc:Name>Supplier SA</cbc:Name>
        </cac:PartyName>
        <cac:PostalAddress>
            <cbc:StreetName>Supplier street 1</cbc:StreetName>
            <cbc:CityName>Antwerpen</cbc:CityName>
            <cbc:PostalZone>2000</cbc:PostalZone>
            <cac:Country>
                <cbc:IdentificationCode listID="ISO3166-1:Alpha2">BE</cbc:IdentificationCode>
            </cac:Country>
        </cac:PostalAddress>
        <cac:PartyTaxScheme>
            <cbc:CompanyID schemeID="BE:VAT">BE0010012675</cbc:CompanyID>
            <cac:TaxScheme>
                <cbc:ID>VAT</cbc:ID>
            </cac:TaxScheme>
        </cac:PartyTaxScheme>
        <cac:PartyLegalEntity>
            <cbc:CompanyID schemeID="BE:VAT">BE0010012675</cbc:CompanyID>
        </cac:PartyLegalEntity>
    </cac:Party>
</cac:AccountingSupplierParty>
```       


#### AccountingCustomerParty

- Party\\EndpointID => "customer_vat": "BE0010022375",
- Party\\PartyName\\Name => "customer_name": "Customer SA",
- Party\\PostalAddress\\StreetName => "customer_address": "Customer street 1",
- Party\\PostalAddress\\CityName => "customer_city": "Liège",
- Party\\PostalAddress\\PostalZone => "customer_postal_code": "4000",
- Party\\PostalAddress\\Country\\IdentificationCode => "customer_country": "BE",
- Party\\PartyTaxScheme\\CompanyID =>  "customer_vat": "BE0010022375",
- Party\\PartyTaxScheme\\TaxScheme\\ID => "VAT" 
- Party\\PartyLegalEntity\\CompanyID =>  "customer_vat": "BE0010022375",

**schemeID="BE:VAT"** is a hardcoded attribute for:
 - Party\\EndpointID  
 - Party\\PartyTaxScheme\\CompanyID  
 - Party\\PartyLegalEntity\\CompanyID  
   

Minimum PayLoad (Customer VAT is not supplied)  : 

```
<cac:AccountingCustomerParty>
        <cac:Party>
            <cac:PartyName>
                <cbc:Name>Customer SA</cbc:Name>
            </cac:PartyName>
        </cac:Party>
</cac:AccountingCustomerParty>
```

```
 <cac:AccountingCustomerParty>
        <cac:Party>
            <cbc:EndpointID schemeID="BE:VAT">BE0010022375</cbc:EndpointID>
            <cac:PartyName>
                <cbc:Name>Customer SA</cbc:Name>
            </cac:PartyName>
            <cac:PostalAddress>
                <cbc:StreetName>Customer street 1</cbc:StreetName>
                <cbc:CityName>Liege</cbc:CityName>
                <cbc:PostalZone>4000</cbc:PostalZone>
                <cac:Country>
                    <cbc:IdentificationCode listID="ISO3166-1:Alpha2">BE</cbc:IdentificationCode>
                </cac:Country>
            </cac:PostalAddress>
            <cac:PartyTaxScheme>
                <cbc:CompanyID schemeID="BE:VAT">BE0010022375</cbc:CompanyID>
                <cac:TaxScheme>
                    <cbc:ID>VAT</cbc:ID>
                </cac:TaxScheme>
            </cac:PartyTaxScheme>
            <cac:PartyLegalEntity>
                <cbc:CompanyID schemeID="BE:VAT">BE0010022375</cbc:CompanyID>
            </cac:PartyLegalEntity>
        </cac:Party>
</cac:AccountingCustomerParty>
```


#### PaymentMeans

- PaymentMeansCode  =>  **<cbc:PaymentMeansCode listID="UNCL4461">1</cbc:PaymentMeansCode>** is hardcoded.
- PaymentDueDate => "invoice_due_date": "2015-12-31" or "invoice_date": "2015-11-06" if no due date.
- PaymentID  => "payment_reference": "501570102394" only if  "payment_reference_is_structured": true 
- PayeeFinancialAccount\\ID => "bank_account_number": "BE03974000000103"  ; **schemeID="IBAN"** is hardcoded
- PayeeFinancialAccount\\FinancialInstitutionBranch\\FinancialInstitution\\ID => "bank_account_bic": "CDBXBE33" ; **schemeID="BIC"** is hardcoded


```
 <cac:PaymentMeans>
    <cbc:PaymentMeansCode listID="UNCL4461">1</cbc:PaymentMeansCode>
    <cbc:PaymentDueDate>2015-12-31</cbc:PaymentDueDate>
    <cac:PayeeFinancialAccount>
        <cbc:ID schemeID="IBAN">BE03974000000103</cbc:ID>
        <cbc:Name/>
        <cac:FinancialInstitutionBranch>
            <cac:FinancialInstitution>
                <cbc:ID schemeID="BIC">CDBXBE33</cbc:ID>
            </cac:FinancialInstitution>
        </cac:FinancialInstitutionBranch>
    </cac:PayeeFinancialAccount>
 </cac:PaymentMeans>
```


```
 <cac:PaymentMeans>
    <cbc:PaymentMeansCode listID="UNCL4461">1</cbc:PaymentMeansCode>
    <cbc:PaymentDueDate>2015-12-31</cbc:PaymentDueDate>
    <cbc:PaymentID>501570102394</cbc:PaymentID>
    <cac:PayeeFinancialAccount>
        <cbc:ID schemeID="IBAN">BE03974000000103</cbc:ID>
        <cbc:Name/>
        <cac:FinancialInstitutionBranch>
            <cac:FinancialInstitution>
                <cbc:ID schemeID="BIC">CDBXBE33</cbc:ID>
            </cac:FinancialInstitution>
        </cac:FinancialInstitutionBranch>
    </cac:PayeeFinancialAccount>
 </cac:PaymentMeans>
```


#### PaymentTerms

if "payment\_reference\_is\_structured": false and payment_reference is not blank then "payment_reference": "501570102394" goes in PaymentTerms\\Note

```
<cac:PaymentTerms>
    <cbc:Note>Reference libre ...</cbc:Note>
</cac:PaymentTerms>
```

#### TaxTotal

- TaxAmount => "invoice_amount_vat": "39.60" "invoice_currency": "EUR  **from invoice payload**
- TaxSubtotal\\TaxableAmount =>  "amount_vat_excluded": "160" "invoice_currency": "EUR
- TaxSubtotal\\TaxAmount =>  "amount_vat": "33.60" "invoice_currency": "EUR 
- TaxSubtotal\\TaxCategory\\ID => "tax_category": "03"  Take the VATCode corresponding to 01 in the tab
- TaxSubtotal\\TaxCategory\\Percent => "tax_category": "03"  Take the VATValue corresponding to 03 in the tab 
- TaxSubtotal\\TaxableAmount =>   "amount_vat_excluded": "100" "invoice_currency": "EUR
- TaxSubtotal\\TaxAmount =>  "amount_vat": "6.00" "invoice_currency": "EUR 
- TaxSubtotal\\TaxCategory\\ID => "tax_category": "01"  Take the VATCode corresponding to 01 in the tab
- TaxSubtotal\\TaxCategory\\Percent => "tax_category": "01"  Take the VATValue corresponding to 01 in the tab


**currencyID="EUR"** Attribute : "invoice_currency": "EUR" in : 

 - TaxAmount
 - TaxSubtotal\\TaxAmount
 - TaxSubtotal\\TaxableAmount
 - TaxSubtotal\\TaxAmount



```
"taxes": [
  {
      "amount_vat_excluded": "160",
      "amount_vat": "33.60",
      "tax_category": "03"
  },
  {
      "amount_vat_excluded": "100",
      "amount_vat": "6.00",
      "tax_category": "01"
  }
]
```

```
<cac:TaxTotal>
    <cbc:TaxAmount currencyID="EUR">39.60</cbc:TaxAmount>
    <cac:TaxSubtotal>
        <cbc:TaxableAmount currencyID="EUR">160.00</cbc:TaxableAmount>
        <cbc:TaxAmount currencyID="EUR">33.60</cbc:TaxAmount>
        <cac:TaxCategory>
            <cbc:ID schemeID="UNCL5305">S</cbc:ID>
            <cbc:Percent>21.0</cbc:Percent>
            <cac:TaxScheme>
                <cbc:ID>VAT</cbc:ID>
            </cac:TaxScheme>
        </cac:TaxCategory>
    </cac:TaxSubtotal>
    <cac:TaxSubtotal>
        <cbc:TaxableAmount currencyID="EUR">100.00</cbc:TaxableAmount>
        <cbc:TaxAmount currencyID="EUR">6.00</cbc:TaxAmount>
        <cac:TaxCategory>
            <cbc:ID schemeID="UNCL5305">AA</cbc:ID>
            <cbc:Percent>6.0</cbc:Percent>
            <cac:TaxScheme>
                <cbc:ID>VAT</cbc:ID>
            </cac:TaxScheme>
        </cac:TaxCategory>
    </cac:TaxSubtotal>
</cac:TaxTotal>
```


#### LegalMonetaryTotal

- LineExtensionAmount => "invoice_amount_vat_excluded": "260.00"
- TaxExclusiveAmount =>   "invoice_amount_vat_excluded": "260.00"
- TaxInclusiveAmount => "invoice_amount": "299.60"
- PayableAmount => "payable_amount": "100"

**currencyID="EUR"** Attribute : "invoice_currency": "EUR" in : 

 - LineExtensionAmount
 - TaxExclusiveAmount
 - TaxInclusiveAmount
 - PayableAmount

```
<cac:LegalMonetaryTotal>
    <cbc:LineExtensionAmount currencyID="EUR">260.00</cbc:LineExtensionAmount>
    <cbc:TaxExclusiveAmount currencyID="EUR">260.00</cbc:TaxExclusiveAmount>
    <cbc:TaxInclusiveAmount currencyID="EUR">299.60</cbc:TaxInclusiveAmount>
    <cbc:PayableAmount currencyID="EUR">100.00</cbc:PayableAmount>
</cac:LegalMonetaryTotal>
```


#### InvoiceLine

 - ID => increment
 - InvoicedQuantity => "quantity": "1.00" => unitCode="C62"????
 - LineExtensionAmount =>  "amount_vat_excluded": "100" "invoice_currency": "EUR
 - TaxTotal\\TaxAmount =>  "invoice_amount_vat": "21.00" "invoice_currency": "EUR
 - AccountingCostCode  =>  "gl_account": "700000"
 - Item\\Name => "description": "First Product"
 - Item\\SellersItemIdentification\\ID =>  "code": "pr01"
 - Item\\ClassifiedTaxCategory\\ID =>  "tax_category": "03"  " : Take the VATCode corresponding to 03 in the tab + **schemeID="UNCL5305"** is hardcoded http://www.unece.org/trade/untdid/d97a/uncl/uncl5305.htm
 - Item\\ClassifiedTaxCategory\\Percent =>  "tax_category": "03"  " : Take the VATValue corresponding to 03 in the tab
 - Price\\PriceAmount => "unit_price": "100"  "invoice_currency": "EUR


**currencyID="EUR"** Attribute : "invoice_currency": "EUR" in : 

 - LineExtensionAmount
 - TaxTotal\\TaxAmount
 - Price\\PriceAmount



```
<cac:InvoiceLine>
    <cbc:ID>1</cbc:ID>
    <cbc:InvoicedQuantity unitCode="C62" unitCodeListID="UNECERec20">1.00</cbc:InvoicedQuantity>
    <cbc:LineExtensionAmount currencyID="EUR ">100.0</cbc:LineExtensionAmount>
    <cac:TaxTotal>
        <cbc:TaxAmount currencyID="EUR">21.00</cbc:TaxAmount>
    </cac:TaxTotal>
    <cbc:AccountingCostCode>700000</cbc:AccountingCostCode>
    <cac:Item>
        <cbc:Name>First Product</cbc:Name>
        <cac:SellersItemIdentification>
            <cbc:ID>pr01</cbc:ID>
        </cac:SellersItemIdentification>
        <cac:ClassifiedTaxCategory>
            <cbc:ID schemeID="UNCL5305">S</cbc:ID>
            <cbc:Percent>21.0</cbc:Percent>
            <cac:TaxScheme>
                <cbc:ID>VAT</cbc:ID>
            </cac:TaxScheme>
        </cac:ClassifiedTaxCategory>
    </cac:Item>
    <cac:Price>
        <cbc:PriceAmount currencyID="EUR">100.0</cbc:PriceAmount>
    </cac:Price>
</cac:InvoiceLine>
```


Description	                   | TaxCategoryCode	|VAT section	   |UNCL5305   |VATValue
-------------------------------|--------------------|------------------|-----------|------------
0%	                           | 00	                |00	               |AA         |0.0
6%	                           | 01	                |01	               |AA         |6.0
12%	                           | 02	                |02	               |AA         |12.0
21%	                           | 03	                |03	               |S          |21.0
Contractor                     | 45	                |45	               |B          |0.0
Sundries excluded from VTA     | NA	                |NA	               |E          |0.0 
Margin (Marge/Marge)	       | MA		            |                  |S or AA    |0.0
0% Clause 44                   | 00/44	            |00	               |E          |0.0 
ICD Goods                      | 46/GO	            |46	               |G          |0.0
ICD Manufacturing cost         | 47/TO	            |47	               |G          |0.0
ICD Assembly                   | 47/AS	            |47	               |G          |0.0
ICD Distance                   | 47/DI	            |47	               |G          |0.0
ICD Services                   | 47/SE	            |47	               |G          |0.0
ICD Triangle                   | 46/TR	            |46	               |G          |0.0
ICD Services B2B               | 44	                |44	               |G          |0.0
Export non E.U.                | 47/EX	            |47	               |G          |0.0
Indirect export                | 47/EI	            |47	               |G          |0.0
Export via E.U.                | 47/EE	            |47	               |G          |0.0
Standard exchange              | 03/SE	            |03	               |S          |0.0


What values are needed  ?

Is TaxCategoryCode sufficient  ?

Are the corresponding values correct ?

Does VATValue should be overridable if VATPercentage is set in other case than 00 - 01 - 02 - 03 ?


http://www.e-fff.be/files/efff_UBL_VATBel_V110_Final.xls

Code |Description
-----|----------------------------------------
A	 |Mixed tax rate	Code specifying that the rate is based on mixed tax.
AA	 |Lower rate	Tax rate is lower than standard rate.
AB	 |Exempt for resale	A tax category code indicating the item is tax exempt when the item is bought for future resale.
AC	 |Value Added Tax (VAT) not now due for payment	A code to indicate that the Value Added Tax (VAT) amount which is due on the current invoice is to be paid on receipt of a separate VAT payment request.
AD	 |Value Added Tax (VAT) due from a previous invoice	A code to indicate that the Value Added Tax (VAT) amount of a previous invoice is to be paid.
B	 |Transferred (VAT)	VAT not to be paid to the issuer of the invoice but directly to relevant tax authority.
C	 |Duty paid by supplier	Duty associated with shipment of goods is paid by the supplier; customer receives goods with duty paid.
E	 |Exempt from tax	Code specifying that taxes are not applicable.
G	 |Free export item, tax not charged	Code specifying that the item is free export and taxes are not charged.
H	 |Higher rate	Code specifying a higher rate of duty or tax or fee.
O	 |Services outside scope of tax	Code specifying that taxes are not applicable to the services
S	 |Standard rate	Code specifying the standard rate.
Z	 |Zero rated goods	Code specifying that the goods are at a zero rate.



## JSON payload

Field                           |Type    |Values - format            |Required ? |Description                                       
----------------------          |--------|---------------------------|:---------:|------------------------------------------------
pdf_upload_id                   |string  |uuid                       |x          |id previously returned after success file upload  
pdf_filename                    |string  |                           |x          |original file name (unique)                       
sha1                            |string  |sha1                       |x          |Secure Hash Algorithm (checksum)                  
supplier_vat                    |string  |BE[0-9]{10}                |x          |Supplier VAT                                      
supplier_name                   |string  |?{1,40}                    |x          |Name of the supplier                              
supplier_address                |string  |?{1,40}                    |           |Address of the supplier                                              
supplier_city                   |string  |?{1,40}                    |           |City of the supplier                              
supplier_postal_code            |string  |?{1,40}                    |           |Postal code of the supplier    
supplier_country                |string  |[A-Z]{2}                   |           |Country of the supplier ISO3166-1:Alpha2          
bank_account_number             |string  |BE[0-9]14                  |           |IBAN number of the supplier                       
bank_account_bic                |string  |[A-Z][0-9]{8,11}           |           |Bic code of the bank of the supplier              
customer_vat                    |string  |                           |           |VAT number of the customer [european vat](http://ec.europa.eu/taxation_customs/vies/faq.html)                       
customer_name                   |string  |?{1,40}                    |x          |Name of the customer                              
customer_address                |string  |?{1,40}                    |           |Address of the customer                                              
customer_city                   |string  |?{1,40}                    |           |City of the customer                              
customer_postal_code            |string  |?{1,40}                    |           |Postal code of the customer    
customer_country                |string  |[A-Z]{2}                   |           |Country of the customer ISO3166-1:Alpha2                                      
invoice_number                  |string  |?{1,40}                    |x          |Invoice Number                                    
invoice_date                    |string  |yyyy-mm-dd                 |x          |Invoice date                                      
invoice_type                    |string  |invoice,credit_note        |x          |type of invoice:invoice or credit_note              
invoice_currency                |string  |EUR\|[A-Z]{3}              |x          |Currency of the invoice                                                                        
invoice_due_date                |string  |yyyy-mm-dd                 |           |Due date of the invoice                         
                                |        |                           |           |If no due date,the invoice date is used    
invoice_description             |string  |?{1,40}                    |           |Description of the invoice                                             
invoice_amount_vat_excluded     |string  |[0-9]{10}.[0-9]{2}         |x          |Total amount of the invoice excluding VAT         
invoice_amount_vat              |string  |[0-9]{10}.[0-9]{2}         |x          |Total amount of VAT  
invoice_amount                  |string  |[0-9]{10}.[0-9]{2}         |x          |Total amount of the invoice including VAT  
payable_amount                  |string  |[0-9]{10}.[0-9]{2}         |           |If an invoice has already been partially          
                                |        |                           |           |paid, the Payable amount could be different than the invoice amount       
payment_reference               |string  |[0-9]{3}/[0-9]{4}/[0-9]{5} |           |Structured reference for the payment (*)             
payment_reference_is_structured |bool    | true,false                |           |default false
lines                           |JSON    |                           |x          |Lines of the invoices (see below)   
taxes                           |JSON    |                           |x          |Lines of the tax (see below)    


**Validation**:

 - invoice_amount_vat_excluded max 2 decimal
 - invoice_amount_vat max 2 decimal
 - invoice_amount max 2 decimal
 - payable_amount max 2 decimal


### UBL Tags

Field                           |Type    | Ubl tag 
--------------------------------|--------|-----------------------------------------------------------------------------
supplier_vat                    |string  |\\AccountingSupplierParty\\Party\\EndpointID
supplier_name                   |string  |\\AccountingSupplierParty\\Party\\PartyName\Name  
supplier_address                |string  |\\AccountingSupplierParty\\Party\\PostalAddress\StreetName             
supplier_city                   |string  |\\AccountingSupplierParty\\Party\\PostalAddress\CityName
supplier_postal_code            |string  |\\AccountingSupplierParty\\Party\\PostalAddress\\PostalZone
supplier_country                |string  |\\AccountingSupplierParty\\Party\\PostalAddress\\Country\\IdentificationCode
bank_account_number             |string  |\\PaymentMeans\PayeeFinancialAccount\\ID
bank_account_bic                |string |\\PaymentMeans\PayeeFinancialAccount\\FinancialInstitutionBranch\\FinancialInstitution\\ID
customer_vat                    |string  |\\AccountingCustomerParty\\Party\\EndpointID
customer_name                   |string  |\\AccountingCustomerParty\\Party\\PartyName\\Name
customer_address                |string  |\\AccountingCustomerParty\\Party\\PostalAddress\\StreetName                 
customer_city                   |string  |\\AccountingCustomerParty\\Party\\PostalAddress\\CityName
customer_postal_code            |string  |\\AccountingCustomerParty\\Party\\PostalAddress\\PostalZone
customer_country                |string  |\\AccountingCustomerParty\\Party\\PostalAddress\\Country\\IdentificationCode  invoice_number                  |string  |\\ID
invoice_date                    |string  |\\IssueDate
invoice_type                    |string  |\\InvoiceTypeCode
invoice_currency                |string  |\\DocumentCurrencyCode                                          
invoice_due_date                |string  |\\PaymentMeans\\PaymentDueDate
invoice_description             |string  |\\Note                   
invoice_amount_vat_excluded     |string  |\\LegalMonetaryTotal\\TaxExclusiveAmount
invoice_amount_vat              |string  |\\TaxTotal\TaxAmount
invoice_amount                  |string  |\\LegalMonetaryTotal\\TaxInclusiveAmount                                      payable_amount                  |string  |\\LegalMonetaryTotal\\PayableAmount
payment_reference               |string  |\\PaymentMeans\\PaymentID (payment_reference_is_structured = true) 
payment_reference_is_structured |bool    |\\PaymentTerms\\Note  (payment_reference_is_structured = false)  			

 
**Note:** : \PaymentMeans\PaymentMeansCode => 1 as default value

# Invoice lines

## JSON payload

Field                |Type    |Values - format            |Required ? |Description                                      
---------------------|--------|-------------------------- |:---------:|-------------------------------------------------
code                 |string  |                           |x          |Item code of the supplier                        
description          |string  |                           |x          |Description of the line                          
gl_account           |string  |                           |           |General Ledger account                           
quantity             |string  |                           |           |Quantity of the line                             
unit_price           |string  |                           |           |Unit price of the item                       amount_vat_excluded  |string  |                           |x          |Amount excluding VAT                           
amount_vat           |string  |                           |x          |Amount of the VAT   
tax_category         |string  |                           |x          |Tab to create


lines exposed invoice details. A least one invoice line is required.

**Validation**:

 - code **or** description is required
 - quantity max 4 decimal
 - Price max 4 decimal
 - vat_percentage max 2 decimal
 - amount_vat : max 2 decimal

**TODO** : tax_category implications on ubl

### UBL tags

Field                |Type    | Ubl tag           
---------------------|--------|-------------------------------------------------------                             
code                 |string  | \\InvoiceLine\\Item\\Name         
description          |string  | \\InvoiceLine\\Item\\Description          
gl_account           |string  | \\InvoiceLine\\AccountingCostCode        
quantity             |string  | \\InvoiceLine\\InvoicedQuantity         
unit_price           |string  | \\InvoiceLine\\Price\\PriceAmount             
amount_vat_excluded  |string  | \\InvoiceLine\\LineExtensionAmount      
vat_percentage       |string  | \\InvoiceLine\\TaxSubtotal\\Percent         
amount_vat           |string  | \\InvoiceLine\\TaxTotal\\TaxAmount
tax_category         |string  | \\InvoiceLine\\Item\\ClassifiedTaxCategory...


# Invoice taxes

## JSON payload

Field                |Type    |Values - format            |Required ? |Description                                      
---------------------|--------|-------------------------- |:---------:|-------------------------------------------------
amount_vat_excluded  |string  |[0-9]{10}.[0-9]{2}         |x          |Amount excluding VAT                        
vat_percentage       |string  |[0-9]{2}.[0-9]{2}          |           |Percentage of the VAT                            
amount_vat           |string  |[0-9]{10}.[0-9]{2}         |x          |Amount of VAT 
tax_category         |string  |[0-9]{10}.[0-9]{2}         |x          |Tab to create


 - At least one tax line is required as for invoice line.
 
### UBL tags

Field                |Type    | Ubl tag                          
---------------------|--------|-------------------------                             
amount_vat_excluded  |string  |\\TaxTotal\\TaxSubtotal\\TaxableAmount                     
vat_percentage       |string  |\\TaxTotal\\TaxSubtotal\\TaxCategory\\Percent                          
amount_vat           |string  |\\TaxTotal\\TaxSubtotal\\TaxAmount
tax_category         |string  |\\TaxTotal\\TaxSubtotal\\TaxCategory\\...



> FULL returned JSON  :

```
{
    "pdf_upload_id": "3cacc5ff-0b25-408c-b519-b4301d89ab8a",
    "pdf_filename": "test.pdf",
    "sha1": "18e950a281def4a5e3840a0fdfae84f08b277424",
    "supplier_vat": "BE0010012675",
    "supplier_name": "Supplier SA",
    "supplier_address": "Supplier street 1",
    "supplier_city": "Antwerpen",
    "supplier_postal_code": "2000",
    "supplier_country": "BE",
    "bank_account_number": "BE03974000000103",
    "bank_account_bic": "CDBXBE33",
    "customer_vat": "BE0010022375",
    "customer_name": "Customer SA",
    "customer_address": "Customer street 1",
    "customer_city": "Liège",
    "customer_postal_code": "4000",
    "customer_country": "BE",
    "invoice_number": "15701023",
    "invoice_date": "2015-11-06",
    "invoice_type": "invoice",
    "invoice_currency": "EUR",
    "invoice_due_date": "2015-12-31",
    "invoice_description": "Description of the invoice",
    "invoice_amount": "299.60",
    "invoice_amount_vat_excluded": "260.00",
    "invoice_amount_vat": "39.60",
    "payable_amount": "100",
    "payment_reference": "501570102394",
    "payment_reference_is_structured": true,
    "lines": [
        {
            "code": "pr01",
            "description": "First Product",
            "gl_account": "700000",
            "quantity": "1.00",
            "unit_price": "100",
            "amount_vat_excluded": "100",
            "vat_percentage": "21.00",
            "amount_vat": "21.00",
            "tax_category": "03"
        },
        {
            "code": "pr02",
            "description": "Second Product",
            "gl_account": "701000",
            "quantity": "2.00",
            "unit_price": "30",
            "amount_vat_excluded": "60",
            "vat_percentage": "21.00",
            "amount_vat": "12.60",
            "tax_category": "03"
        },
        {
            "code": "pr03",
            "description": "Third Product",
            "gl_account": "701000",
            "quantity": "1.00",
            "unit_price": "100",
            "amount_vat_excluded": "100",
            "vat_percentage": "6.00",
            "amount_vat": "6.00",
            "tax_category": "01"
        }
    ],
    "taxes": [
        {
            "vat_percentage": "21.00",
            "amount_vat_excluded": "160",
            "amount_vat": "33.60",
            "tax_category": "03"
        },
        {
            "vat_percentage": "6.00",
            "amount_vat_excluded": "100",
            "amount_vat": "6.00",
            "tax_category": "01"
        }
    ]
}
```
