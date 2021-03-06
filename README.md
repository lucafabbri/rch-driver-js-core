# API Reference

## Core
**Kind**: global class  

* [Core](#markdown-header-core)
    * [new Core(isSerial)](#markdown-header-new-coreisserial)
    * [.header()](#markdown-header-coreheader)
    * [.footer()](#markdown-header-corefooter)
    * [.cmd(protocolCommand)](#markdown-header-corecmdprotocolcommand)
    * [.parseBool(value)](#markdown-header-coreparseboolvalue-number) ⇒ number
    * [.subtotal()](#markdown-header-coresubtotal)
    * [.clear()](#markdown-header-coreclear)
    * [.cancel()](#markdown-header-corecancel)
    * [.transfer()](#markdown-header-coretransfer)
    * [.paperPeekOut()](#markdown-header-corepaperpeekout)
    * [.departmentSell(departmentId, description, value, [qty], [sellType])](#markdown-header-coredepartmentselldepartmentid-description-value-qty-selltype-string) ⇒ string
    * [.departmentSellFromLineItem(lineItem)](#markdown-header-coredepartmentsellfromlineitemlineitem)
    * [.returnGoods(date, closure, number, [onlyCheck])](#markdown-header-corereturngoodsdate-closure-number-onlycheck-string) ⇒ string
    * [.returnGoodsFromDTO(returnInfo)](#markdown-header-corereturngoodsfromdtoreturninfo-string) ⇒ string
    * [.lottery(code)](#markdown-header-corelotterycode)
    * [.discountPercentage(percentage, description)](#markdown-header-corediscountpercentagepercentage-description)
    * [.increasePercentage(percentage, description)](#markdown-header-coreincreasepercentagepercentage-description)
    * [.discountValue(value, description)](#markdown-header-corediscountvaluevalue-description)
    * [.increaseValue(value, description)](#markdown-header-coreincreasevaluevalue-description)
    * [.increaseValueSubtotal(value, description)](#markdown-header-coreincreasevaluesubtotalvalue-description)
    * [.openNonFiscalReceipt(cutPaper, heading)](#markdown-header-coreopennonfiscalreceiptcutpaper-heading)
    * [.closeNonFiscalReceipt()](#markdown-header-coreclosenonfiscalreceipt)
    * [.payment(paymentId, value, description)](#markdown-header-corepaymentpaymentid-value-description)
    * [.paymentFromPaymentItem(paymentItem)](#markdown-header-corepaymentfrompaymentitempaymentitem-string) ⇒ string
    * [.returnReceipt(date, closure, number, onlyCheck, serialNumber)](#markdown-header-corereturnreceiptdate-closure-number-onlycheck-serialnumber)
    * [.returnReceiptFromDTO(returnInfo)](#markdown-header-corereturnreceiptfromdtoreturninfo)
    * [.getLastReceipt()](#markdown-header-coregetlastreceipt)
    * [.giftReceipt()](#markdown-header-coregiftreceipt)
    * [.operator(operatorId)](#markdown-header-coreoperatoroperatorid)
    * [.closeReceipt()](#markdown-header-coreclosereceipt)
    * [.terminateOperation()](#markdown-header-coreterminateoperation)
    * [.printRow(content)](#markdown-header-coreprintrowcontent)
    * [.printRowAfterTotal(content)](#markdown-header-coreprintrowaftertotalcontent)
    * [.printRowBeforeFiscalContent(content)](#markdown-header-coreprintrowbeforefiscalcontentcontent)
    * [.printFiscalCode(fiscalCode)](#markdown-header-coreprintfiscalcodefiscalcode)
    * [.reg()](#markdown-header-corereg)
    * [.x()](#markdown-header-corex)
    * [.z()](#markdown-header-corez)
    * [.prg()](#markdown-header-coreprg)
    * [.srv()](#markdown-header-coresrv)
    * [.xReport()](#markdown-header-corexreport)
    * [.zReport()](#markdown-header-corezreport)
    * [.restart()](#markdown-header-corerestart)
    * [.updateOnDemand()](#markdown-header-coreupdateondemand)
    * [.sendPendingXmls()](#markdown-header-coresendpendingxmls)
    * [.testXmlUrl()](#markdown-header-coretestxmlurl)
    * [.displayMessage(rowId, message)](#markdown-header-coredisplaymessagerowid-message)
    * [.printBarCode(type, code)](#markdown-header-coreprintbarcodetype-code)
    * [.printBarCode_UpcE(code)](#markdown-header-coreprintbarcode_upcecode)
    * [.printBarCode_Ean13(code)](#markdown-header-coreprintbarcode_ean13code)
    * [.printBarCode_Ean8(code)](#markdown-header-coreprintbarcode_ean8code)
    * [.printBarCode_Code39(code)](#markdown-header-coreprintbarcode_code39code)
    * [.printBarCode_UpcA(code)](#markdown-header-coreprintbarcode_upcacode)
    * [.printBarCode_Itf(code)](#markdown-header-coreprintbarcode_itfcode)
    * [.printBarCode_Codabar(code)](#markdown-header-coreprintbarcode_codabarcode)
    * [.printBarCode_Code128(code)](#markdown-header-coreprintbarcode_code128code)
    * [.printBarCode_Code93(code)](#markdown-header-coreprintbarcode_code93code)
    * [.printBarCode_QRCode(code)](#markdown-header-coreprintbarcode_qrcodecode)
    * [.dgfeStatus()](#markdown-header-coredgfestatus)
    * [.periodicAssessmentStatus()](#markdown-header-coreperiodicassessmentstatus)
    * [.inactivityAndPendings()](#markdown-header-coreinactivityandpendings)
    * [.dgfeFreeSpace()](#markdown-header-coredgfefreespace)
    * [.deviceStatus()](#markdown-header-coredevicestatus)
    * [.printerStatus()](#markdown-header-coreprinterstatus)
    * [.getSerialNumber()](#markdown-header-coregetserialnumber)
    * [.getFirmwareRevision()](#markdown-header-coregetfirmwarerevision)
    * [.rtStatus()](#markdown-header-corertstatus)
    * [.pendingXmlStatus()](#markdown-header-corependingxmlstatus)
    * [.inServiceStatus()](#markdown-header-coreinservicestatus)
    * [.allProgramming()](#markdown-header-coreallprogramming)
    * [.C125(vat_on_ticket)](#markdown-header-corec125vat_on_ticket)
    * [.C126(midnight_alert)](#markdown-header-corec126midnight_alert)
    * [.C132(print_register_number)](#markdown-header-corec132print_register_number)
    * [.C133(subtotal_required)](#markdown-header-corec133subtotal_required)
    * [.C135(max_receipt_amount)](#markdown-header-corec135max_receipt_amount)
    * [.C136(change_on_payments)](#markdown-header-corec136change_on_payments)
    * [.C138(department_net)](#markdown-header-corec138department_net)
    * [.C170(rt_print_appendix, rt_enable_appendix_Cut)](#markdown-header-corec170rt_print_appendix-rt_enable_appendix_cut)
    * [.C451(date)](#markdown-header-corec451date)
    * [.C452(date)](#markdown-header-corec452date)
    * [.C917(invoice_on_receipt_enable, receipt_print_on_2_lines, invoice_subtotal_enable, invoice_disable_check_client, invoice_print_unit_price)](#markdown-header-corec917invoice_on_receipt_enable-receipt_print_on_2_lines-invoice_subtotal_enable-invoice_disable_check_client-invoice_print_unit_price)
    * [.C918(id, name)](#markdown-header-corec918id-name)
    * [.C927(print_unit_price, print_single_quantity)](#markdown-header-corec927print_unit_price-print_single_quantity)
    * [.C928(disable_double_feed)](#markdown-header-corec928disable_double_feed)
    * [.C932(print_with_buffering)](#markdown-header-corec932print_with_buffering)
    * [.C980(notify_cash)](#markdown-header-corec980notify_cash)
    * [.C997(enabled_cutter)](#markdown-header-corec997enabled_cutter)
    * [.H(headingRow, description)](#markdown-header-corehheadingrow-description)
    * [.t(courtesyRow, description)](#markdown-header-coretcourtesyrow-description)
    * [.O(operatorId, name)](#markdown-header-coreooperatorid-name)
    * [.R(deptId, price, vat, name, halo, lalo, single, grp_code, dpt_type)](#markdown-header-corerdeptid-price-vat-name-halo-lalo-single-grp_code-dpt_type)
    * [.T(paymentId, name, change, cash, pay_discount, tender_credit_type, opendrawer, input_total_amount, ticket)](#markdown-header-coretpaymentid-name-change-cash-pay_discount-tender_credit_type-opendrawer-input_total_amount-ticket)
    * [.U(department_discount)](#markdown-header-coreudepartment_discount)
    * [.V(vatId, rate_type, value, ateco_code)](#markdown-header-corevvatid-rate_type-value-ateco_code)
    * [.dptTypeStringToInt(val)](#markdown-header-coredpttypestringtointval)
    * [.dptIntToTypeString(val)](#markdown-header-coredptinttotypestringval)
    * [.rateStringToInt(value)](#markdown-header-coreratestringtointvalue)
    * [.natureStringToInt(value)](#markdown-header-corenaturestringtointvalue)
    * [.creditStringToInt(tender_credit_type)](#markdown-header-corecreditstringtointtender_credit_type)
    * [.creditIntToString(tender_credit_type)](#markdown-header-corecreditinttostringtender_credit_type)

### new Core(isSerial)
<p>Constructor default is for WebService</p>


| Param | Type | Default |
| --- | --- | --- |
| isSerial | Boolean | `true` | 

### core.header()
<p>Builds the main header for the request</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.footer()
<p>Build the footer for the request</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.cmd(protocolCommand)
<p>Encapsulte the command in the xml 'cmd' tag</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| protocolCommand | String | 

### core.parseBool(value) ⇒ number
<p>Convert boolean value to 0 and 1
false = 0
true = 1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 2:18:03 AM  

| Param | Type |
| --- | --- |
| value | boolean | 

### core.subtotal()
<p>Create the subtotal command =S</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.clear()
<p>Create the clear command =K</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.cancel()
<p>Create the cancel(Annullo) command =a</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.transfer()
<p>Create the transfer(storno) command =s</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.paperPeekOut()
<p>Create the paper peek out command(avanzamento scontrino) =f</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.departmentSell(departmentId, description, value, [qty], [sellType]) ⇒ string
<p>Creates  a Department Sell command e.g. =R1/$1000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:51:45 AM  

| Param | Type | Default |
| --- | --- | --- |
| departmentId | number |  | 
| description | string |  | 
| value | number |  | 
| [qty] | number | `1` | 
| [sellType] | SellType |  | 

### core.departmentSellFromLineItem(lineItem)
<p>Creates  a Department Sell command from LineItemDTO e.g. =R1/$1000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| lineItem | LineItemDTO | 

### core.returnGoods(date, closure, number, [onlyCheck]) ⇒ string
<p>Opens a return document or check only if it is possibile. IF onlyCheck is false it triggers autoopen if check is ok</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:52:14 AM  

| Param | Type |
| --- | --- |
| date | Date | 
| closure | number | 
| number | number | 
| [onlyCheck] | boolean | 

### core.returnGoodsFromDTO(returnInfo) ⇒ string
<p>Opens a return document or check only if it is possibile. IF onlyCheck is false it triggers autoopen if check is ok</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:52:45 AM  

| Param | Type |
| --- | --- |
| returnInfo | ReturnInfoDTO | 

### core.lottery(code)
<p>Add the lottery code to the receipt e.g. =&quot;/?L/$1/(F1234567)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.discountPercentage(percentage, description)
<p>Create the discount command e.g. =%-/*12.15
Percentage is rounded to 2 digits</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| percentage | Number | 
| description | String | 

### core.increasePercentage(percentage, description)
<p>Create the increase command e.g. =%+/*12.15
Percentage is rounded to 2 digits</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| percentage | Number | 
| description | String | 

### core.discountValue(value, description)
<p>Create the discount value command e.g. =V-/*12.15</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | Number | 
| description | String | 

### core.increaseValue(value, description)
<p>Create the increase value command e.g. =V+/*12.15</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | Number | 
| description | String | 

### core.increaseValueSubtotal(value, description)
<p>Create the increase value command e.g. =V+/*12.15 after subtotal =S</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | Number | 
| description | String | 

### core.openNonFiscalReceipt(cutPaper, heading)
<p>Open the non fiscal receipt =o</p>
<p>header == null =&gt; Full header
header == false =&gt; No Header
header == true =&gt; Only first Header row</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| cutPaper | Boolean | 
| heading | Boolean ⎮ null | 

### core.closeNonFiscalReceipt()
<p>Close the non fiscal receipt =o</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.payment(paymentId, value, description)
<p>Create the payment command e.g. =T3/$2000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| paymentId | Number | 
| value | Number | 
| description | String ⎮ null | 

### core.paymentFromPaymentItem(paymentItem) ⇒ string
<p>Create the payment command e.g. =T3/$2000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:54:00 AM  

| Param | Type |
| --- | --- |
| paymentItem | PaymentItemDTO | 

### core.returnReceipt(date, closure, number, onlyCheck, serialNumber)
<p>Return a receipt providing date closure and number, if onlyCheck is set then checks if true and check&amp;run if false</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| date | String | 
| closure | Number | 
| number | Number | 
| onlyCheck |  | 
| serialNumber |  | 

### core.returnReceiptFromDTO(returnInfo)
<p>Return a receipt providing date closure and number, if onlyCheck is set then checks if true and check&amp;run if false</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| returnInfo | ReturnInfoDTO | 

### core.getLastReceipt()
<p>get the last document printed</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.giftReceipt()
<p>command to print the last receipt without the amounts of the articles, called “Receipt Gift &quot;(in REG)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.operator(operatorId)
<p>Create the operator command e.g. =O1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| operatorId | Number | 

### core.closeReceipt()
<p>Create the receipt close command =c</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.terminateOperation()
<p>Terminates the current operation =x</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.printRow(content)
<p>Create the command for alfanumeric rows =&quot;/?A/(Prova stampa alfanumerica)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| content | String ⎮ RowDTO | 

### core.printRowAfterTotal(content)
<p>Create the command for alfanumeric rows after total =”/&amp;1/(descrizione 35 chars)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| content | String | 

### core.printRowBeforeFiscalContent(content)
<p>Create the command for alfanumeric rows before fiscal content =&quot;/(stringa alfanumerica)/&amp;1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| content | String | 

### core.printFiscalCode(fiscalCode)
<p>Create the command for printing Fiscal Code =&quot;/?C/(01033470251)
The fiscal code is not check in its format</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| fiscalCode | String | 

### core.reg()
<p>Enter in reg key =C1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.x()
<p>Enter in x report key =C2</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.z()
<p>Enter in z report key =C3</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.prg()
<p>Enter in prog key =C4</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.srv()
<p>Enter in service key =C5</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.xReport()
<p>Read daily situation (x report)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.zReport()
<p>Do fiscal closure (z report)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.restart()
<p>Restart the printer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.updateOnDemand()
<p>Send the update on demand command</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.sendPendingXmls()
<p>Try resend pending XML</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.testXmlUrl()
<p>Test Agenzia delle Entrate endpoint</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.displayMessage(rowId, message)
**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| rowId | Number | 
| message | String | 

### core.printBarCode(type, code)
<p>Create the Create BarCode command =&quot;/$2/(4006381333641)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| type | Number | 
| code | String | 

### core.printBarCode_UpcE(code)
<p>Create BarCode of type: UPC-E</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Ean13(code)
<p>Create BarCode of type: EAN-13</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Ean8(code)
<p>Create BarCode of type: EAN-8</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Code39(code)
<p>Create BarCode of type: CODE-39</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_UpcA(code)
<p>Create BarCode of type: UPC-A</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Itf(code)
<p>Create BarCode of type: ITF</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Codabar(code)
<p>Create BarCode of type: CODABAR</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Code128(code)
<p>Create BarCode of type: CODE-128</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Code93(code)
<p>Create BarCode of type: CODE-93</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_QRCode(code)
<p>Create BarCode of type: QR CODE</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.dgfeStatus()
<p>Get the DGFE Status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.periodicAssessmentStatus()
<p>Send the periodic assessment command</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.inactivityAndPendings()
<p>Send the inactivity and pendings command</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.dgfeFreeSpace()
<p>Check DGFE free space</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.deviceStatus()
<p>Verify the status of print &lt;&lt;?s</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.printerStatus()
<p>Check the printer status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.getSerialNumber()
<p>Device Serial number &lt;&lt;/?m</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.getFirmwareRevision()
<p>Device Firware Revision &lt;&lt;/?f</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.rtStatus()
<p>Check RT status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.pendingXmlStatus()
<p>Check pending XML status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.inServiceStatus()
<p>Check if the RT is in service</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.allProgramming()
<p>Get all programming</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.C125(vat_on_ticket)
<p>Program a the Vat on ticket</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| vat_on_ticket | Boolean | 

### core.C126(midnight_alert)
<p>Program the midnight alert</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| midnight_alert | Boolean | 

### core.C132(print_register_number)
<p>program the print of the register number</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| print_register_number | Boolean | 

### core.C133(subtotal_required)
<p>Program id the subtotal is required</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| subtotal_required | Boolean | 

### core.C135(max_receipt_amount)
<p>Program the maximum receipt amount</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| max_receipt_amount | Number | 

### core.C136(change_on_payments)
<p>Program the change on payments</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| change_on_payments | Boolean | 

### core.C138(department_net)
<p>Program the deprtment net</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| department_net | Boolean | 

### core.C170(rt_print_appendix, rt_enable_appendix_Cut)
<p>Program the appendix in the rt</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| rt_print_appendix | Boolean | 
| rt_enable_appendix_Cut | Boolean | 

### core.C451(date)
<p>Download DGFE data at specific date format DDMMYY e.g. 010121 (January 1st 2021)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| date | String | 

### core.C452(date)
<p>Download DGFE data at specific date format DDMMYY e.g. 010121 (January 1st 2021)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| date | String | 

### core.C917(invoice_on_receipt_enable, receipt_print_on_2_lines, invoice_subtotal_enable, invoice_disable_check_client, invoice_print_unit_price)
<p>Program the invoice on the rt</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| invoice_on_receipt_enable | Boolean | 
| receipt_print_on_2_lines | Boolean | 
| invoice_subtotal_enable | Boolean | 
| invoice_disable_check_client | Boolean | 
| invoice_print_unit_price | Boolean | 

### core.C918(id, name)
<p>Program one specific header line &gt;C918/*1/$1/(Testo max 48 caratteri)
text is trimmed and equally spaced to center the content</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| id | Number | 
| name | String | 

### core.C927(print_unit_price, print_single_quantity)
<p>Program unit price and single quantity</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| print_unit_price | Boolean | 
| print_single_quantity | Boolean | 

### core.C928(disable_double_feed)
<p>Program the disable double feed</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| disable_double_feed | Boolean | 

### core.C932(print_with_buffering)
<p>Program the print with buffering</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| print_with_buffering | Boolean | 

### core.C980(notify_cash)
<p>Program the notify cash</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| notify_cash | Boolean | 

### core.C997(enabled_cutter)
<p>Enables the cutter</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| enabled_cutter | Boolean | 

### core.H(headingRow, description)
<p>Program the heading rows (0-6)
and the Invoice heading rows (7-13)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| headingRow | Number | 
| description | String | 

### core.t(courtesyRow, description)
<p>Program the cortesy lines rows (0-2)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| courtesyRow | Number | 
| description | String | 

### core.O(operatorId, name)
<p>Program an operator</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| operatorId | Number | 
| name | String | 

### core.R(deptId, price, vat, name, halo, lalo, single, grp_code, dpt_type)
<p>Program a Department</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| deptId | Number | 
| price | Number | 
| vat | Number | 
| name | String | 
| halo | Number | 
| lalo | Number | 
| single | Boolean | 
| grp_code | Number ⎮ null | 
| dpt_type | String | 

### core.T(paymentId, name, change, cash, pay_discount, tender_credit_type, opendrawer, input_total_amount, ticket)
<p>Program a payment</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| paymentId | Number | 
| name | String | 
| change | Boolean | 
| cash | Boolean | 
| pay_discount | Boolean | 
| tender_credit_type | String | 
| opendrawer | Boolean | 
| input_total_amount | Boolean | 
| ticket | Boolean | 

### core.U(department_discount)
<p>Program department discount</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| department_discount | Boolean | 

### core.V(vatId, rate_type, value, ateco_code)
<p>Program a vat</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| vatId | Number | 
| rate_type | String | 
| value | Number | 
| ateco_code | String | 

### core.dptTypeStringToInt(val)
<p>Util to convert Department type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| val | String | 

### core.dptIntToTypeString(val)
<p>Util to convert Department type int to string</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| val | Number | 

### core.rateStringToInt(value)
<p>Util to convert rate type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | String | 

### core.natureStringToInt(value)
<p>Util to convert nature type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | String | 

### core.creditStringToInt(tender_credit_type)
<p>Util to convert credit type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| tender_credit_type | String | 

### core.creditIntToString(tender_credit_type)
<p>Util to convert credit type integer to string</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| tender_credit_type | Number | 

## BarCodeType : enum
<p>BarCode Types</p>

**Kind**: global enum  
**Date**: 1/11/2022 - 10:07:11 AM  
## BillType : enum
<p>Enum the Bill Types</p>

**Kind**: global enum  
**Date**: 1/11/2022 - 10:11:25 AM  
## SellType : enum
<p>The SellType of a BillItem</p>

**Kind**: global enum  
**Date**: 1/11/2022 - 10:52:47 AM  
**See**: LineItemDTO
## Core : [Core](#markdown-header-new-coreisserial)
<p>Core builder of commands</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 1:59:01 AM  

* [Core](#markdown-header-core-core) : [Core](#markdown-header-core-core)
    * [new Core(isSerial)](#markdown-header-new-coreisserial)
    * [.header()](#markdown-header-coreheader)
    * [.footer()](#markdown-header-corefooter)
    * [.cmd(protocolCommand)](#markdown-header-corecmdprotocolcommand)
    * [.parseBool(value)](#markdown-header-coreparseboolvalue-number) ⇒ number
    * [.subtotal()](#markdown-header-coresubtotal)
    * [.clear()](#markdown-header-coreclear)
    * [.cancel()](#markdown-header-corecancel)
    * [.transfer()](#markdown-header-coretransfer)
    * [.paperPeekOut()](#markdown-header-corepaperpeekout)
    * [.departmentSell(departmentId, description, value, [qty], [sellType])](#markdown-header-coredepartmentselldepartmentid-description-value-qty-selltype-string) ⇒ string
    * [.departmentSellFromLineItem(lineItem)](#markdown-header-coredepartmentsellfromlineitemlineitem)
    * [.returnGoods(date, closure, number, [onlyCheck])](#markdown-header-corereturngoodsdate-closure-number-onlycheck-string) ⇒ string
    * [.returnGoodsFromDTO(returnInfo)](#markdown-header-corereturngoodsfromdtoreturninfo-string) ⇒ string
    * [.lottery(code)](#markdown-header-corelotterycode)
    * [.discountPercentage(percentage, description)](#markdown-header-corediscountpercentagepercentage-description)
    * [.increasePercentage(percentage, description)](#markdown-header-coreincreasepercentagepercentage-description)
    * [.discountValue(value, description)](#markdown-header-corediscountvaluevalue-description)
    * [.increaseValue(value, description)](#markdown-header-coreincreasevaluevalue-description)
    * [.increaseValueSubtotal(value, description)](#markdown-header-coreincreasevaluesubtotalvalue-description)
    * [.openNonFiscalReceipt(cutPaper, heading)](#markdown-header-coreopennonfiscalreceiptcutpaper-heading)
    * [.closeNonFiscalReceipt()](#markdown-header-coreclosenonfiscalreceipt)
    * [.payment(paymentId, value, description)](#markdown-header-corepaymentpaymentid-value-description)
    * [.paymentFromPaymentItem(paymentItem)](#markdown-header-corepaymentfrompaymentitempaymentitem-string) ⇒ string
    * [.returnReceipt(date, closure, number, onlyCheck, serialNumber)](#markdown-header-corereturnreceiptdate-closure-number-onlycheck-serialnumber)
    * [.returnReceiptFromDTO(returnInfo)](#markdown-header-corereturnreceiptfromdtoreturninfo)
    * [.getLastReceipt()](#markdown-header-coregetlastreceipt)
    * [.giftReceipt()](#markdown-header-coregiftreceipt)
    * [.operator(operatorId)](#markdown-header-coreoperatoroperatorid)
    * [.closeReceipt()](#markdown-header-coreclosereceipt)
    * [.terminateOperation()](#markdown-header-coreterminateoperation)
    * [.printRow(content)](#markdown-header-coreprintrowcontent)
    * [.printRowAfterTotal(content)](#markdown-header-coreprintrowaftertotalcontent)
    * [.printRowBeforeFiscalContent(content)](#markdown-header-coreprintrowbeforefiscalcontentcontent)
    * [.printFiscalCode(fiscalCode)](#markdown-header-coreprintfiscalcodefiscalcode)
    * [.reg()](#markdown-header-corereg)
    * [.x()](#markdown-header-corex)
    * [.z()](#markdown-header-corez)
    * [.prg()](#markdown-header-coreprg)
    * [.srv()](#markdown-header-coresrv)
    * [.xReport()](#markdown-header-corexreport)
    * [.zReport()](#markdown-header-corezreport)
    * [.restart()](#markdown-header-corerestart)
    * [.updateOnDemand()](#markdown-header-coreupdateondemand)
    * [.sendPendingXmls()](#markdown-header-coresendpendingxmls)
    * [.testXmlUrl()](#markdown-header-coretestxmlurl)
    * [.displayMessage(rowId, message)](#markdown-header-coredisplaymessagerowid-message)
    * [.printBarCode(type, code)](#markdown-header-coreprintbarcodetype-code)
    * [.printBarCode_UpcE(code)](#markdown-header-coreprintbarcode_upcecode)
    * [.printBarCode_Ean13(code)](#markdown-header-coreprintbarcode_ean13code)
    * [.printBarCode_Ean8(code)](#markdown-header-coreprintbarcode_ean8code)
    * [.printBarCode_Code39(code)](#markdown-header-coreprintbarcode_code39code)
    * [.printBarCode_UpcA(code)](#markdown-header-coreprintbarcode_upcacode)
    * [.printBarCode_Itf(code)](#markdown-header-coreprintbarcode_itfcode)
    * [.printBarCode_Codabar(code)](#markdown-header-coreprintbarcode_codabarcode)
    * [.printBarCode_Code128(code)](#markdown-header-coreprintbarcode_code128code)
    * [.printBarCode_Code93(code)](#markdown-header-coreprintbarcode_code93code)
    * [.printBarCode_QRCode(code)](#markdown-header-coreprintbarcode_qrcodecode)
    * [.dgfeStatus()](#markdown-header-coredgfestatus)
    * [.periodicAssessmentStatus()](#markdown-header-coreperiodicassessmentstatus)
    * [.inactivityAndPendings()](#markdown-header-coreinactivityandpendings)
    * [.dgfeFreeSpace()](#markdown-header-coredgfefreespace)
    * [.deviceStatus()](#markdown-header-coredevicestatus)
    * [.printerStatus()](#markdown-header-coreprinterstatus)
    * [.getSerialNumber()](#markdown-header-coregetserialnumber)
    * [.getFirmwareRevision()](#markdown-header-coregetfirmwarerevision)
    * [.rtStatus()](#markdown-header-corertstatus)
    * [.pendingXmlStatus()](#markdown-header-corependingxmlstatus)
    * [.inServiceStatus()](#markdown-header-coreinservicestatus)
    * [.allProgramming()](#markdown-header-coreallprogramming)
    * [.C125(vat_on_ticket)](#markdown-header-corec125vat_on_ticket)
    * [.C126(midnight_alert)](#markdown-header-corec126midnight_alert)
    * [.C132(print_register_number)](#markdown-header-corec132print_register_number)
    * [.C133(subtotal_required)](#markdown-header-corec133subtotal_required)
    * [.C135(max_receipt_amount)](#markdown-header-corec135max_receipt_amount)
    * [.C136(change_on_payments)](#markdown-header-corec136change_on_payments)
    * [.C138(department_net)](#markdown-header-corec138department_net)
    * [.C170(rt_print_appendix, rt_enable_appendix_Cut)](#markdown-header-corec170rt_print_appendix-rt_enable_appendix_cut)
    * [.C451(date)](#markdown-header-corec451date)
    * [.C452(date)](#markdown-header-corec452date)
    * [.C917(invoice_on_receipt_enable, receipt_print_on_2_lines, invoice_subtotal_enable, invoice_disable_check_client, invoice_print_unit_price)](#markdown-header-corec917invoice_on_receipt_enable-receipt_print_on_2_lines-invoice_subtotal_enable-invoice_disable_check_client-invoice_print_unit_price)
    * [.C918(id, name)](#markdown-header-corec918id-name)
    * [.C927(print_unit_price, print_single_quantity)](#markdown-header-corec927print_unit_price-print_single_quantity)
    * [.C928(disable_double_feed)](#markdown-header-corec928disable_double_feed)
    * [.C932(print_with_buffering)](#markdown-header-corec932print_with_buffering)
    * [.C980(notify_cash)](#markdown-header-corec980notify_cash)
    * [.C997(enabled_cutter)](#markdown-header-corec997enabled_cutter)
    * [.H(headingRow, description)](#markdown-header-corehheadingrow-description)
    * [.t(courtesyRow, description)](#markdown-header-coretcourtesyrow-description)
    * [.O(operatorId, name)](#markdown-header-coreooperatorid-name)
    * [.R(deptId, price, vat, name, halo, lalo, single, grp_code, dpt_type)](#markdown-header-corerdeptid-price-vat-name-halo-lalo-single-grp_code-dpt_type)
    * [.T(paymentId, name, change, cash, pay_discount, tender_credit_type, opendrawer, input_total_amount, ticket)](#markdown-header-coretpaymentid-name-change-cash-pay_discount-tender_credit_type-opendrawer-input_total_amount-ticket)
    * [.U(department_discount)](#markdown-header-coreudepartment_discount)
    * [.V(vatId, rate_type, value, ateco_code)](#markdown-header-corevvatid-rate_type-value-ateco_code)
    * [.dptTypeStringToInt(val)](#markdown-header-coredpttypestringtointval)
    * [.dptIntToTypeString(val)](#markdown-header-coredptinttotypestringval)
    * [.rateStringToInt(value)](#markdown-header-coreratestringtointvalue)
    * [.natureStringToInt(value)](#markdown-header-corenaturestringtointvalue)
    * [.creditStringToInt(tender_credit_type)](#markdown-header-corecreditstringtointtender_credit_type)
    * [.creditIntToString(tender_credit_type)](#markdown-header-corecreditinttostringtender_credit_type)

### new Core(isSerial)
<p>Constructor default is for WebService</p>


| Param | Type | Default |
| --- | --- | --- |
| isSerial | Boolean | `true` | 

### core.header()
<p>Builds the main header for the request</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.footer()
<p>Build the footer for the request</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.cmd(protocolCommand)
<p>Encapsulte the command in the xml 'cmd' tag</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| protocolCommand | String | 

### core.parseBool(value) ⇒ number
<p>Convert boolean value to 0 and 1
false = 0
true = 1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 2:18:03 AM  

| Param | Type |
| --- | --- |
| value | boolean | 

### core.subtotal()
<p>Create the subtotal command =S</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.clear()
<p>Create the clear command =K</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.cancel()
<p>Create the cancel(Annullo) command =a</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.transfer()
<p>Create the transfer(storno) command =s</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.paperPeekOut()
<p>Create the paper peek out command(avanzamento scontrino) =f</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.departmentSell(departmentId, description, value, [qty], [sellType]) ⇒ string
<p>Creates  a Department Sell command e.g. =R1/$1000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:51:45 AM  

| Param | Type | Default |
| --- | --- | --- |
| departmentId | number |  | 
| description | string |  | 
| value | number |  | 
| [qty] | number | `1` | 
| [sellType] | SellType |  | 

### core.departmentSellFromLineItem(lineItem)
<p>Creates  a Department Sell command from LineItemDTO e.g. =R1/$1000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| lineItem | LineItemDTO | 

### core.returnGoods(date, closure, number, [onlyCheck]) ⇒ string
<p>Opens a return document or check only if it is possibile. IF onlyCheck is false it triggers autoopen if check is ok</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:52:14 AM  

| Param | Type |
| --- | --- |
| date | Date | 
| closure | number | 
| number | number | 
| [onlyCheck] | boolean | 

### core.returnGoodsFromDTO(returnInfo) ⇒ string
<p>Opens a return document or check only if it is possibile. IF onlyCheck is false it triggers autoopen if check is ok</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:52:45 AM  

| Param | Type |
| --- | --- |
| returnInfo | ReturnInfoDTO | 

### core.lottery(code)
<p>Add the lottery code to the receipt e.g. =&quot;/?L/$1/(F1234567)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.discountPercentage(percentage, description)
<p>Create the discount command e.g. =%-/*12.15
Percentage is rounded to 2 digits</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| percentage | Number | 
| description | String | 

### core.increasePercentage(percentage, description)
<p>Create the increase command e.g. =%+/*12.15
Percentage is rounded to 2 digits</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| percentage | Number | 
| description | String | 

### core.discountValue(value, description)
<p>Create the discount value command e.g. =V-/*12.15</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | Number | 
| description | String | 

### core.increaseValue(value, description)
<p>Create the increase value command e.g. =V+/*12.15</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | Number | 
| description | String | 

### core.increaseValueSubtotal(value, description)
<p>Create the increase value command e.g. =V+/*12.15 after subtotal =S</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | Number | 
| description | String | 

### core.openNonFiscalReceipt(cutPaper, heading)
<p>Open the non fiscal receipt =o</p>
<p>header == null =&gt; Full header
header == false =&gt; No Header
header == true =&gt; Only first Header row</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| cutPaper | Boolean | 
| heading | Boolean ⎮ null | 

### core.closeNonFiscalReceipt()
<p>Close the non fiscal receipt =o</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.payment(paymentId, value, description)
<p>Create the payment command e.g. =T3/$2000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| paymentId | Number | 
| value | Number | 
| description | String ⎮ null | 

### core.paymentFromPaymentItem(paymentItem) ⇒ string
<p>Create the payment command e.g. =T3/$2000</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
**Date**: 1/11/2022 - 1:54:00 AM  

| Param | Type |
| --- | --- |
| paymentItem | PaymentItemDTO | 

### core.returnReceipt(date, closure, number, onlyCheck, serialNumber)
<p>Return a receipt providing date closure and number, if onlyCheck is set then checks if true and check&amp;run if false</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| date | String | 
| closure | Number | 
| number | Number | 
| onlyCheck |  | 
| serialNumber |  | 

### core.returnReceiptFromDTO(returnInfo)
<p>Return a receipt providing date closure and number, if onlyCheck is set then checks if true and check&amp;run if false</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| returnInfo | ReturnInfoDTO | 

### core.getLastReceipt()
<p>get the last document printed</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.giftReceipt()
<p>command to print the last receipt without the amounts of the articles, called “Receipt Gift &quot;(in REG)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.operator(operatorId)
<p>Create the operator command e.g. =O1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| operatorId | Number | 

### core.closeReceipt()
<p>Create the receipt close command =c</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.terminateOperation()
<p>Terminates the current operation =x</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.printRow(content)
<p>Create the command for alfanumeric rows =&quot;/?A/(Prova stampa alfanumerica)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| content | String ⎮ RowDTO | 

### core.printRowAfterTotal(content)
<p>Create the command for alfanumeric rows after total =”/&amp;1/(descrizione 35 chars)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| content | String | 

### core.printRowBeforeFiscalContent(content)
<p>Create the command for alfanumeric rows before fiscal content =&quot;/(stringa alfanumerica)/&amp;1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| content | String | 

### core.printFiscalCode(fiscalCode)
<p>Create the command for printing Fiscal Code =&quot;/?C/(01033470251)
The fiscal code is not check in its format</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| fiscalCode | String | 

### core.reg()
<p>Enter in reg key =C1</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.x()
<p>Enter in x report key =C2</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.z()
<p>Enter in z report key =C3</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.prg()
<p>Enter in prog key =C4</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.srv()
<p>Enter in service key =C5</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.xReport()
<p>Read daily situation (x report)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.zReport()
<p>Do fiscal closure (z report)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.restart()
<p>Restart the printer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.updateOnDemand()
<p>Send the update on demand command</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.sendPendingXmls()
<p>Try resend pending XML</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.testXmlUrl()
<p>Test Agenzia delle Entrate endpoint</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.displayMessage(rowId, message)
**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| rowId | Number | 
| message | String | 

### core.printBarCode(type, code)
<p>Create the Create BarCode command =&quot;/$2/(4006381333641)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| type | Number | 
| code | String | 

### core.printBarCode_UpcE(code)
<p>Create BarCode of type: UPC-E</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Ean13(code)
<p>Create BarCode of type: EAN-13</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Ean8(code)
<p>Create BarCode of type: EAN-8</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Code39(code)
<p>Create BarCode of type: CODE-39</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_UpcA(code)
<p>Create BarCode of type: UPC-A</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Itf(code)
<p>Create BarCode of type: ITF</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Codabar(code)
<p>Create BarCode of type: CODABAR</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Code128(code)
<p>Create BarCode of type: CODE-128</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_Code93(code)
<p>Create BarCode of type: CODE-93</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.printBarCode_QRCode(code)
<p>Create BarCode of type: QR CODE</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| code | String | 

### core.dgfeStatus()
<p>Get the DGFE Status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.periodicAssessmentStatus()
<p>Send the periodic assessment command</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.inactivityAndPendings()
<p>Send the inactivity and pendings command</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.dgfeFreeSpace()
<p>Check DGFE free space</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.deviceStatus()
<p>Verify the status of print &lt;&lt;?s</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.printerStatus()
<p>Check the printer status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.getSerialNumber()
<p>Device Serial number &lt;&lt;/?m</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.getFirmwareRevision()
<p>Device Firware Revision &lt;&lt;/?f</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.rtStatus()
<p>Check RT status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.pendingXmlStatus()
<p>Check pending XML status</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.inServiceStatus()
<p>Check if the RT is in service</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.allProgramming()
<p>Get all programming</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  
### core.C125(vat_on_ticket)
<p>Program a the Vat on ticket</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| vat_on_ticket | Boolean | 

### core.C126(midnight_alert)
<p>Program the midnight alert</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| midnight_alert | Boolean | 

### core.C132(print_register_number)
<p>program the print of the register number</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| print_register_number | Boolean | 

### core.C133(subtotal_required)
<p>Program id the subtotal is required</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| subtotal_required | Boolean | 

### core.C135(max_receipt_amount)
<p>Program the maximum receipt amount</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| max_receipt_amount | Number | 

### core.C136(change_on_payments)
<p>Program the change on payments</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| change_on_payments | Boolean | 

### core.C138(department_net)
<p>Program the deprtment net</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| department_net | Boolean | 

### core.C170(rt_print_appendix, rt_enable_appendix_Cut)
<p>Program the appendix in the rt</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| rt_print_appendix | Boolean | 
| rt_enable_appendix_Cut | Boolean | 

### core.C451(date)
<p>Download DGFE data at specific date format DDMMYY e.g. 010121 (January 1st 2021)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| date | String | 

### core.C452(date)
<p>Download DGFE data at specific date format DDMMYY e.g. 010121 (January 1st 2021)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| date | String | 

### core.C917(invoice_on_receipt_enable, receipt_print_on_2_lines, invoice_subtotal_enable, invoice_disable_check_client, invoice_print_unit_price)
<p>Program the invoice on the rt</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| invoice_on_receipt_enable | Boolean | 
| receipt_print_on_2_lines | Boolean | 
| invoice_subtotal_enable | Boolean | 
| invoice_disable_check_client | Boolean | 
| invoice_print_unit_price | Boolean | 

### core.C918(id, name)
<p>Program one specific header line &gt;C918/*1/$1/(Testo max 48 caratteri)
text is trimmed and equally spaced to center the content</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| id | Number | 
| name | String | 

### core.C927(print_unit_price, print_single_quantity)
<p>Program unit price and single quantity</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| print_unit_price | Boolean | 
| print_single_quantity | Boolean | 

### core.C928(disable_double_feed)
<p>Program the disable double feed</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| disable_double_feed | Boolean | 

### core.C932(print_with_buffering)
<p>Program the print with buffering</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| print_with_buffering | Boolean | 

### core.C980(notify_cash)
<p>Program the notify cash</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| notify_cash | Boolean | 

### core.C997(enabled_cutter)
<p>Enables the cutter</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| enabled_cutter | Boolean | 

### core.H(headingRow, description)
<p>Program the heading rows (0-6)
and the Invoice heading rows (7-13)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| headingRow | Number | 
| description | String | 

### core.t(courtesyRow, description)
<p>Program the cortesy lines rows (0-2)</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| courtesyRow | Number | 
| description | String | 

### core.O(operatorId, name)
<p>Program an operator</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| operatorId | Number | 
| name | String | 

### core.R(deptId, price, vat, name, halo, lalo, single, grp_code, dpt_type)
<p>Program a Department</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| deptId | Number | 
| price | Number | 
| vat | Number | 
| name | String | 
| halo | Number | 
| lalo | Number | 
| single | Boolean | 
| grp_code | Number ⎮ null | 
| dpt_type | String | 

### core.T(paymentId, name, change, cash, pay_discount, tender_credit_type, opendrawer, input_total_amount, ticket)
<p>Program a payment</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| paymentId | Number | 
| name | String | 
| change | Boolean | 
| cash | Boolean | 
| pay_discount | Boolean | 
| tender_credit_type | String | 
| opendrawer | Boolean | 
| input_total_amount | Boolean | 
| ticket | Boolean | 

### core.U(department_discount)
<p>Program department discount</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| department_discount | Boolean | 

### core.V(vatId, rate_type, value, ateco_code)
<p>Program a vat</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| vatId | Number | 
| rate_type | String | 
| value | Number | 
| ateco_code | String | 

### core.dptTypeStringToInt(val)
<p>Util to convert Department type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| val | String | 

### core.dptIntToTypeString(val)
<p>Util to convert Department type int to string</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| val | Number | 

### core.rateStringToInt(value)
<p>Util to convert rate type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | String | 

### core.natureStringToInt(value)
<p>Util to convert nature type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| value | String | 

### core.creditStringToInt(tender_credit_type)
<p>Util to convert credit type string to integer</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| tender_credit_type | String | 

### core.creditIntToString(tender_credit_type)
<p>Util to convert credit type integer to string</p>

**Kind**: instance method of [Core](#markdown-header-new-coreisserial)  

| Param | Type |
| --- | --- |
| tender_credit_type | Number | 

## BillDTO : BillDTO
<p>Interface of a Bill including Receipts, Returns and Cancel Documents</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 10:10:12 AM  

* [BillDTO](#markdown-header-billdto-billdto) : [BillDTO](#markdown-header-billdto-billdto)
    * [.isReturn](#markdown-header-billdtoisreturn-boolean) : boolean
    * [.isCancel](#markdown-header-billdtoiscancel-boolean) : boolean
    * [.isReceipt](#markdown-header-billdtoisreceipt-boolean) : boolean

### billDTO.isReturn : boolean
<p>This is true if the BillType is a RETURN</p>

**Kind**: instance property of [BillDTO](#markdown-header-billdto-billdto)  
**Read only**: true  
**Date**: 1/11/2022 - 10:12:52 AM  
### billDTO.isCancel : boolean
<p>This is true if the BillType is a CANCEL</p>

**Kind**: instance property of [BillDTO](#markdown-header-billdto-billdto)  
**Read only**: true  
**Date**: 1/11/2022 - 10:14:08 AM  
### billDTO.isReceipt : boolean
<p>This is true if the BillType is a RECEIPT</p>

**Kind**: instance property of [BillDTO](#markdown-header-billdto-billdto)  
**Read only**: true  
**Date**: 1/11/2022 - 10:14:45 AM  
## DiscountDTO : DiscountDTO
<p>Discount information applied to a BillItem</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 10:17:38 AM  
**See**: BillItemDTO
## LineItemDTO : LineItemDTO
<p>Information of a BillItem in a Bill</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 10:19:19 AM  
**See**: BillDTO
## PaymentItemDTO : PaymentItemDTO
<p>The Payment details</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 10:29:11 AM  
**See**: BillDTO
## ReturnInfoDTO : ReturnInfoDTO
<p>Mandatory information for a RETURN or CANCEL document issue</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 10:33:57 AM  
**See**: BillDTO
## RowDTO : RowDTO
<p>This is a row of simple text to print in a non fiscal document</p>

**Kind**: global typedef  
**Date**: 1/11/2022 - 10:37:05 AM  
### RowDTO.fromString(value) ⇒ RowDTO
<p>Create a RowDTo from a string.
the string can be plain strings or formatted as follows to include details about barCodeType and size:</p>

**Kind**: static method of RowDTO  
**Date**: 1/11/2022 - 10:47:39 AM  

| Param | Type |
| --- | --- |
| value | string | 

**Example**  
```jsconst simpleRow = 'yoursimplerow';const rowDoubleSize = 'yourtextgoeshere||1'; // Double sizeconst barCode = 'thecode|11 //barcode types between 1 to 11```

* * *
