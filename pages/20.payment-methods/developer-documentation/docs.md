---
title: 'Developer Documentation'
taxonomy:
    category:
        - docs
visible: true
---

## Sellacious Payment Plugin Developer Documentation

In a very basic way a payment process can be represented as below:

1. Your payment plugin supports one or more “**Handler**” each having their own way of processing payment **Authorisation** and **Capturing**.

2. Site Administrator / Shop Owner creates a **Payment Method** in sellacious backend by choosing one of the available Handlers.

3. Your plugin can ask for additional configuration values for each payment method separately. These values will be available to the plugin using `$this->getParams()` during payment processing. These parameters are usually the API Key and Token etc as required by the Payment Gateway.

4. User selects a Payment Method and Enters the Payment Information (if any) required by the plugin.

5. Sellacious calls the relevant Payment Methods Handler Plugin

6. The plugin determines and collects the required values like user information, order information or whatever it needs, from the system.

7. The plugin redirects the user to the Payment Gateway for Authorisation.

8. Payment Gateway redirects the user back to the website with SUCCESS / FAIL / CANCEL status. This is called the Callback action.

9. If the payment was Authorised by the gateway, the plugin will then execute the Payment Capture.

### Glossary

**Payment Plugin:** 
The Joomla extension of type “plugin” and group “sellaciouspayment” that is installed on the sellacious website.


**Payment Handler:**
A unique identifier to identify the payment gateway/process so that sellacious can call the appropriate plugin when a user initiates a payment. A single plugin may implement more than one handlers and implement different payment process for each of them independently. This is useful when your payment gateway supports multiple payment systems. Usually one plugin will implement only one “handler” under normal scenario.


**Payment Method:**
The Payment Options provided to the Customer / Payer to choose from in order to make a payment on your sellacious website. Each payment method is bound to a payment handler, and can have its own configuration settings. This allows your plugin to be independently used with multiple payment gateway credentials as well, depending on which method the user selects.


**Payment Configuration:**
 This is the configuration settings entered by the Shop owner (or whoever creates a payment method) for each payment method. These settings usually are the Gateway API Access Key, API Token, API Passwords etc.


**Payment Information:**
These are the values submitted by the end customer in order to make the payment after selecting a payment method. These can be their Credit Card information, Bank Information, or whatever information the plugin may want to ask from the customer before making a payment.


**Payment Authorisation:**
This is the process where the Plugin redirects the User to Payment Gateway / Banks website to obtain their consent for making payments. The gateway / bank may then require the user to login to their website or enter a secure password, or an OTP (a secret one time password) or whatever they need to verify the user. This entire process after the redirection is not relevant to the plugin. Therefore you need not worry about that part at all.

After the gateway / bank has verified the user and obtained their approval for the payment, it will redirect them back to the website with appropriate Status Code, Authorisation Key, Transaction number etc. In case of failure or cancelled by user, the response would usually contain suitable error code and error message that needs to be handled by the plugin.


**Payment Capturing:**
Once the payment has been authorised, the plugin may need to explicitly charge the customers Card / Bank Account. You need to consult the documentation of the relevant gateway documentation to know whether you need explicit Capturing.


**Payment Gateway Callback:**
The redirection by the payment gateway with the Authorisation response data, with appropriate status, message and Transaction Id etc. Which can be further processed by the plugin.

There are two types of callbacks:

**Callback** – Stateful callback. 
This is performed within the same session in which the payment was initiated and processed. This is the most common type of callback used.

**Feedback** – Stateless callback.
This type of callback is implemented in a few payment gateways to notify your website about the payment status using a separate HTTP request other than the redirection. This request does not contain any session information such as logged in user, browser, etc. Make sure you include any important parameter (such as payment_id, handler name) in the callback URL so that you can identify the transaction for which the feedback is received.

**Payment Validation:**
This is additional security measure supported by some payment gateways that can be used to validate the response obtained by the gateway after the Authorisation process.



Plugin Directory Structure

Example: plg_sellaciouspayment_example

|-- forms/
   |-- fields/
   |-- rules/
   |-- example_handler.xml
|-- images/
   |-- example_handler.jpg
|-- language/
   |-- en-GB/
       |-- en-GB.plg_sellaciouspayment_example.ini
       |-- en-GB.plg_sellaciouspayment_example.sys.ini
|-- libraries/
|-- tmpl/
   |-- default.php
|-- example.php
|-- example.xml


Forms folder is for the xml form which will be loaded for the customer to enter the Payment Information. The filename of the xml should match the supported handler name. One xml each should be placed for each supported handler.
The optional “fields” and “rules” folder can be used to put any custom field type and validation rules. See JFormRule, JFormField for more details.
The “images” folder holds at least one image for the payment handler that may be used by sellacious to represent the payment handlers. Filename must match the handler name with extension “.jpg”. Any additional images required by the plugin should also be put in this folder only.
 The “language” folder is the common language folder as supported by Joomla. It should contain at least one folder “en-GB” and two file in it with the specified name. Additional languages may be added using same file naming convention. Please do not include <language> tag in the plugin installer manifest.
The optional “libraries” folder holds the external library files / classes (e.g. - SDK) that your plugin may need. The directory structure inside this folder depends on your specific needs and the source where the SDK is obtained from. Sellacious does not control or load the contents of this folder. Your plugin is responsible to load the library as and when needed.
The “tmpl” folder holds the layout files that will be used to render HTML output. You will use $this->renderLayout('default', $data); syntax to load a layout named “default.php” from this folder. The template developers will be able to override this in their template. The $this variable will be available in this layout file and it will point to the plugin object itself. Therefore you can use $this to use any of the plugin methods and variables directly within the layout file. The passed $data will be available inside the layout as $displayData.
The files “example.php” and “example.xml” are the plugin class file and plugin installer manifest respectively.
Please do not forget to add the entries of these files and folders in the plugin installer manifest.
Please do not include <language> tag in the plugin installer manifest.


Afterwards you can create ZIP archive with these files and your plugin is ready to install.

Important Notes
The plugin manifest includes the <config> section which will be used to display the Payment Configuration form to the admin / shop owner when creating the Payment Method using one of your plugins’ handlers. You can add the fields in this section to obtain the API credentials and any other information specific to each payment method.
Some Payment Gateway does not require a separate Capture mechanism. They will Authorise and Capture simultaneously.
Some Payment Gateway supports Payment Verification / Validation after the Callback. If this is the case make sure you make use of this feature so that the response cannot be tampered in between.
Some Payment Gateway does not require a redirection at all. They would simply need you to collect the Payment Information from the User (such as Credit Card Details) and pass to the Gateway using CURL etc internally. If this is the case with your plugin, then you don’t need to implement Callback system.
If your plugin requires a redirect and callback mechanism as explained above, you can supply the Callback URL to the gateways as below:
$callbackUrl = $this->getCallbackUrl();
$feedbackUrl = $this->getCallbackUrl(array(), true);
	This will return something like (not exactly, please DO NOT hardcode this URL ever in your plugins):
	http://yourdomain.com/index.php?option=com_sellacious&task=payment.callback
If you need additional parameters in the callback URL such as “status=success” then call this method as below:
$callbackUrl = $this->getCallbackUrl(array('status' => 'success'));
$feedbackUrl = $this->getCallbackUrl(array('status' => 'success'), true);
For a detailed documentation for each plugin function / method, please refer to the attached sample plugin and read the doc-blocks and comments in each method.


Contents of Payment information form XML viz. /forms/xample_handler.xml is:
<?xml version="1.0" encoding="utf-8"?>
<form>
  <fieldset name="payment">
     <fields name="example_handler">
		<!-- The form fields for payment information form goes here -->
     </fields>
  </fieldset>
</form>


You manifest file would look like:
<?xml version="1.0" encoding="utf-8"?>
<extension version="3.0" type="plugin" group="sellaciouspayment" method="upgrade">
  <name>plg_sellaciouspayment_example</name>
  <author>Izhar Aazmi</author>
  <creationDate>November 06, 2017</creationDate>
  <copyright>Copyright (C) 2017 Bhartiy Web Technologies. All rights reserved.</copyright>
  <license>GNU General Public License version 2 or later; see LICENSE.txt</license>
  <authorEmail>info@bhartiy.com</authorEmail>
  <authorUrl>www.bhartiy.com</authorUrl>
  <version>1.0.0</version>
  <description>PLG_SELLACIOUSPAYMENT_EXAMPLE_XML_DESCRIPTION</description>
  <files>
     <folder>forms</folder>
     <folder>images</folder>
     <folder>language</folder>
     <folder>libraries</folder>
     <folder>tmpl</folder>
     <filename plugin="example">example.php</filename>
  </files>
  <config>
     <fields name="params">
        <fieldset name="basic">
           <field
              name="api_mode"
              type="radio"
              default="sandbox"
              description="PLG_SELLACIOUSPAYMENT_EXAMPLE_API_MODE_DESC"
              label="PLG_SELLACIOUSPAYMENT_EXAMPLE_API_MODE_LABEL"
           >
              <option value="live">PLG_SELLACIOUSPAYMENT_EXAMPLE_MODE_LIVE</option>
              <option value="sandbox">PLG_SELLACIOUSPAYMENT_EXAMPLE_MODE_SANDBOX</option>
           </field>
           <field
              name="merchant_code"
              type="text"
              required="true"
              description="PLG_SELLACIOUSPAYMENT_EXAMPLE_MERCHANT_CODE_DESC"
              label="PLG_SELLACIOUSPAYMENT_EXAMPLE_MERCHANT_CODE_LABEL"
              class="inputbox"
           />
           <field
              name="merchant_key"
              type="text"
              required="true"
              description="PLG_SELLACIOUSPAYMENT_EXAMPLE_MERCHANT_KEY_DESC"
              label="PLG_SELLACIOUSPAYMENT_EXAMPLE_MERCHANT_KEY_LABEL"
              class="inputbox"
           />
        </fieldset>
     </fields>
  </config>
</extension>



If your plugin requires redirection and callback mechanism, then your initPayment() method would look similar to this:
/**
* Initiate the payment process
*
* @param   stdClass  $invoice  The data required by the gateway
*
* @return  void
*
* @throws  Exception
*
* @since   1.0.0
*/
protected function initPayment($invoice)
{
  $api         = $this->getApiContext();
  $callbackUrl = $this->getCallbackUrl(array('status' => 'success'));
  $feedbackUrl = $this->getCallbackUrl(array(), true);

  // You can perform the tasks relevant to the plugin's payment process. 
  // How to set the callback URLs depends on the gateway you are working for.

  // Assuming $api->gateway_url is the gateway URL
  $this->app->redirect($api->gateway_url);
}

And you will execute the payment after the callback return

If your plugin does NOT requires redirection and callback mechanism, then your initPayment() method would look similar to this:
/**
* Initiate the payment process
*
* @param   stdClass  $invoice  The data required by the gateway
*
* @return  void
*
* @throws  Exception
*
* @since   1.0.0
*/
protected function initPayment($invoice)
{
  $api         = $this->getApiContext();
  $callbackUrl = $this->getCallbackUrl(array('status' => 'success'));
  $feedbackUrl = $this->getCallbackUrl(array(), true);

  // You can perform the tasks relevant to the plugin's payment process. 
  // How to set the callback URLs depends on the gateway you are working for.

  // If a redirection is not needed you can directly execute payment here.
  $response = $this->executePayment();
  $result   = $this->handleResponse($response);

  return $result;
}


The Plugin Class file
For your reference a full documented plugin file content is given below. Please note that this is an example plugin file, and contains few empty blocks that needs to be implemented depending on the payment gateway you are working for. This example plugin will NOT run as is. Use this as a guide only to create your own sellacious payment plugin. 

The example.php : (The PHP file will be provided separately as attachment as well)
<?php
/**
* @version     1.0.0
* @package     Sellacious Payment - Example
*
* @copyright   Copyright (C) 2017. Bhartiy Web Technologies. All rights reserved.
* @license     GNU General Public License version 2 or later; see LICENSE.txt
* @author      Izhar Aazmi <info@bhartiy.com> - http://www.bhartiy.com
*/
// No direct access.
defined('_JEXEC') or die;

use Joomla\Registry\Registry;

JLoader::import('sellacious.loader');

/**
* Plugin to manage payment via 'example' for sellacious shops checkout process
*
* @subpackage  Example - Sellacious Payments
*
* @since   1.0.0
*/
class plgSellaciousPaymentExample extends SellaciousPluginPayment
{
  /**
   * Returns handlers to the payment methods that will be managed by this plugin
   *
   * @param   string  $context    The calling context, must be 'com_sellacious.payment' to effect
   * @param   array   &$handlers  ByRef, associative array of handlers
   *
   * @return  bool
   *
   * @since   1.0.0
   */
  public function onCollectHandlers($context, array &$handlers)
  {
     if ($context == 'com_sellacious.payment')
     {
        $handlers['example_handler'] = JText::_('PLG_SELLACIOUSPAYMENT_EXAMPLE_API_EXAMPLE_HANDLER');
     }

     return true;
  }

  /**
   * Validates given payment method against this filter.
   * Used to check whether it is okay to show this payment method to user to choose for payment.
   *
   * @param   string    $context  The context identifier:
   *                              'com_sellacious.paymentmethod.cart' OR 'com_sellacious.paymentmethod.addfund'
   * @param   Registry  $method   Registry object for the payment method to test against
   * @param   int       $orderId  The order id/transaction id etc, whatever is relevant for the said context
   *
   * @return  bool
   *
   * @since   1.0.0
   */
  public function onBeforeLoadPaymentMethod($context, Registry $method, $orderId = 0)
  {
     if ($context == 'com_sellacious.paymentmethod.cart' || $context == 'com_sellacious.paymentmethod.addfund')
     {
        if ($method->get('handler') == 'example_handler')
        {
           /**
            * Decide whether all prerequisites to use this payment method is fulfilled,
            * Such as API configuration set, user is authorised to use this method etc.
            *
            * Return true / false based on this decision
            */
        }
     }

     return true;
  }

  /**
   * This method is called when a user selects this payment method for making a payment.
   * This will be the first thing to be called to handover the payment control to a payment plugin.
   * Prior calling this method the order for which this payment is being made would be created in the database.
   *
   * @param   string  $context  The calling context, must be 'com_sellacious.payment' to effect
   *
   * @return  bool
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  public function onRequestPayment($context)
  {
     // You should set the payment property at the very beginning of a call to avoid any collision.
     $paymentId     = $this->getState('id');
     $this->payment = $this->helper->payment->getItem($paymentId);

     // Get a list of supported handlers by this plugin
     $handlers = array();

     $this->onCollectHandlers($context, $handlers);

     // Match the selected handler with the supported ones
     if (!array_key_exists($this->payment->handler, $handlers))
     {
        return true;
     }

     // Collect all the required information for the payment processing
     $invoice = $this->getInvoice();

     if (!$invoice)
     {
        throw new Exception(JText::_('PLG_SELLACIOUSPAYMENT_EXAMPLE_CONTEXT_IS_NOT_VALID'));
     }

     // Execute the payment routine with the collected data
     $this->initPayment($invoice);

     return true;
  }

  /**
   * Callback handler to execute after gateway approval callback (Authorisation)
   *
   * @param   string  $context  The calling context, must be 'com_sellacious.payment' to effect
   *
   * @return  bool
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  public function onPaymentCallback($context)
  {
     // You should set the payment property at the very beginning of a call to avoid any collision.
     $paymentId     = $this->getState('id');
     $this->payment = $this->helper->payment->getItem($paymentId);
     $result        = true;

     if ($context == 'com_sellacious.payment' && $this->payment->handler == 'example_handler')
     {
        $response = $this->executePayment();
        $result   = $this->handleResponse($response);
     }

     return $result;
  }

  /**
   * Feedback handler to execute after gateway approval (Authorisation) or on a payment notification from gateway
   *
   * @param   string  $context  The calling context, must be 'com_sellacious.payment' to effect
   *
   * @return  void
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  public function onPaymentFeedback($context)
  {
     // You should set the payment property at the very beginning of a call to avoid any collision.
     // This is a stateless call, therefore we cannot use getState()
     $paymentId     = $this->app->input->getInt('payment_id');
     $this->payment = $this->helper->payment->getItem($paymentId);

     // IMPORTANT: Set state value for stateless calls, else 'saveResponse' call would fail
     $this->setState('id', $paymentId);

     if ($context == 'com_sellacious.payment' && $this->payment->handler == 'example_handler')
     {
        /**
         * Handle the response as appropriate.
         * If needed and suitable you may call {@see  executePayment()} and {@see  handleResponse()}
         */
     }
  }

  /**
   * Sellacious do not bother about the details a plugin might need.
   * Plugins are set free to fetch what they want. However basic data is directly accessible.
   *
   * @return  stdClass  All the required details for the transaction execution with the Payment Gateway
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  protected function getInvoice()
  {
     $invoice = new stdClass;

     // Implement this to gather all the information that is need for the payment. 
     // E.g. - Payment Amount, User information etc.

     return $invoice;
  }

  /**
   * Initialize SDK configurations using client key and secret with additional connection settings
   *
   * @return  stdClass  The API configuration values
   *
   * @throws  Exception  If the configuration is not set or is invalid
   *
   * @since   1.0.0
   */
  protected function getApiContext()
  {
     $config  = $this->getParams();
     $sandbox = $config->get('api_mode') == 'sandbox';

     $config->set('sandbox', $sandbox);

     // Prepare and preprocess the configuration data as needed
     $api = $config->toObject();

     return $api;
  }

  /**
   * Initiate the payment process
   * The app will have to redirect the buyer to the gateway website, obtain their consent to the payment
   * and subsequently execute the payment using the execute API call.
   *
   * @param   stdClass  $invoice  The data required by the payment gateway to execute the transaction
   *
   * @return  void
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  protected function initPayment($invoice)
  {
     $api         = $this->getApiContext();
     $callbackUrl = $this->getCallbackUrl(array('status' => 'success'));
     $feedbackUrl = $this->getCallbackUrl(array(), true);

     // You can perform the tasks relevant to the plugin's payment process.
     // How to set the callback URLs depends on the gateway you are working for.

     $this->app->redirect($api->gateway_url);
  }

  /**
   * Capture the authorized payment with the API.
   *
   * @return  mixed
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  protected function executePayment()
  {
     // Collect all response data returned by the gateway
     $response = new stdClass;

     // If a CAPTURE is needed do it here and obtain the final response

     // Return the final response for response handler to evaluate
     return $response;
  }

  /**
   * Evaluate the final gateway response and update the payments table appropriately
   *
   * @param   stdClass  $response  The response data returned by {@see  executePayment()}
   *
   * @return  bool
   *
   * @throws  Exception
   *
   * @since   1.0.0
   */
  protected function handleResponse($response)
  {
     $api = $this->getApiContext();

     /**
      * Call {@see  saveResponse()} with the appropriate values either from response directly
      * or creating the values logically based on response.
      */
     $code    = 'THE RESPONSE CODE';
     $status  = 'THE RESPONSE STATUS';
     $message = 'THE RESPONSE MESSAGE';
     $txn_id  = 'THE GATEWAY TRANSACTION ID';

     /**
      * The data variable should contain the entire response except any sensitive information 
      * such as Credit Card information.
      */
     $data  = (array) $response;

     /**
      * The state variable should be set to one of the following constants as suitable.
      * 
      * STATUS_PENDING | STATUS_ABORTED | STATUS_DECLINED | STATUS_AUTHORIZED |
      * STATUS_APPROVAL_HOLD | STATUS_APPROVED
      */
     $state = static::STATUS_APPROVED;

     $this->saveResponse($code, $status, $message, $data, $txn_id, $state, $api->sandbox);

     // Return true if transaction was approved or held for approval, else return false.

     return $state == static::STATUS_APPROVED || $state == static::STATUS_APPROVAL_HOLD;
  }
}