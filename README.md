# [Plugin hangle](https://github.com/annihilatoratm/magento-doc?tab=readme-ov-file#plugin-for-magento-1x-for-pay-by-payneteasy)
# [User registration](https://github.com/annihilatoratm/magento-doc/blob/main/doc-eng.md#user-registration)
# [Payment Flow](https://github.com/annihilatoratm/magento-doc/blob/main/doc-eng.md#payment-flow-1)


## Plugin for Magento 1.x for pay by PaynetEasy

### Available functions

This plugin allows merchant to make payments via [merchant PaynetEasy API](http://wiki.payneteasy.com/index.php/PnE:Merchant_API). These payment methods are available at the moment:
- [x] [Sale Transactions](http://wiki.payneteasy.com/index.php/PnE:Sale_Transactions)
- [ ] [Preauth/Capture Transactions](http://wiki.payneteasy.com/index.php/PnE:Preauth/Capture_Transactions)
- [ ] [Transfer Transactions](http://wiki.payneteasy.com/index.php/PnE:Transfer_Transactions)
- [ ] [Return Transactions](http://wiki.payneteasy.com/index.php/PnE:Return_Transactions)
- [ ] [Recurrent Transactions](http://wiki.payneteasy.com/index.php/PnE:Recurrent_Transactions)
- [x] [Payment Form Integration](http://wiki.payneteasy.com/index.php/PnE:Payment_Form_integration)
- [ ] [Buy Now Button integration](http://wiki.payneteasy.com/index.php/PnE:Buy_Now_Button_integration)
- [ ] [eCheck integration](http://wiki.payneteasy.com/index.php/PnE:eCheck_integration)
- [ ] [Western Union Integration](http://wiki.payneteasy.com/index.php/PnE:Western_Union_Integration)
- [ ] [Bitcoin Integration](http://wiki.payneteasy.com/index.php/PnE:Bitcoin_integration)
- [ ] [Loan Integration](http://wiki.payneteasy.com/index.php/PnE:Loan_integration)
- [ ] [Qiwi Integration](http://wiki.payneteasy.com/index.php/PnE:Qiwi_integration)
- [ ] [Merchant Callbacks](http://wiki.payneteasy.com/index.php/PnE:Merchant_Callbacks)

### System requirements

* PHP 5.3 - 5.5
* [Curl extension](http://php.net/manual/en/book.curl.php)
* [Magento](http://www.magentocommerce.com/download) 1.x (plugin was tested with 1.7)

### <a name="get_package"></a> Getting plugin package

#### Package assembling
1. [Install composer](http://getcomposer.org/doc/00-intro.md), if it is not installed already
2. Clone plugin’s repository: `composer create-project payneteasy/php-plugin-magento --stability=dev --prefer-dist`
3. Go to plugin’s folder: `cd php-plugin-magento`
4. Pack plugin to archive: `composer archive --format=zip`

### Installing plugin

1. [Get plugin package](#get_package)
2. Extract package to Magento’s root folder

### Configuring plugin

1. Go to Magento’s admin panel
2. Go to Stores (1) -> Condiguration (2)

  <img src="/images/magento-1-2.png" width=60% height=60%>
3. Sales (1) -> Payment Method (2)

  <img src="/images/magento-1-1.png" width=60% height=60%>
4. Configure plugin
    1. Fill in the form with plugin settings
    2. Save plugin settings (See picture)



### Uninstalling plugin

In order to uninstall this plugin, the folders and files listed below should be deleted. Paths are relevant to Magento’s root folder:

* `app/code/local/PaynetEasy/`
* `app/design/frontend/base/default/template/paynet/`
* `app/etc/modules/PaynetEasy_Paynet.xml`
* `lib/composer/`
* `lib/payneteasy/`
* `lib/autoload.php`
  
  ## User registration (Optional)
  
  Click on *Create an Account* to start the User registration process. Please fill all required parameters and press on *Create an Account* button to finish registration.

  <img src="/images/magento-register-1.png" width=60% height=60%>
  <img src="/images/magento-register-2.png" width=60% height=60%>
  <img src="/images/magento-register-3.png" width=60% height=60%>

  ## Payment Flow

  1. On the main page click on *main product* to choose the product. Press on *Add to Cart* (1-2) button to add selected item to the Shopping Cart. Once the item was added to the cart, the payment flow can be started. Press on *Proceed to Checkout* (3) to continue.

  <img src="/images/magento-1.png" width=60% height=60%>
  <img src="/images/magento-3.png" width=60% height=60%>
  
  2. Fill all required parameters in the Shipping details window and press *Next*. On the Review & Payments window the order can be processed. **PAYNET** as a Payment Method has to be chosen. Press on *Order payment* to continue.

  <img src="/images/magento-4.png" width=60% height=60%>
  <img src="/images/magento-5.png" width=60% height=60%>

  3. On **Payneteasy Payment Form** all Credit Card information must be set. Once done, press on *Process payment* button. Wait for finish of the payment. 

  <img src="/images/magento-6.png" width=60% height=60%>
  <img src="/images/magento-7.png" width=60% height=60%>
