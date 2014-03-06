# Magento - Customize Price Filter extension

## Forked by @michelem09
This is a fork to give compatibility versus Magento 1.5.1.0 too.

## Overview
Magento is able to display price ranges in the layered navigation. It offers 3 ways to calculate price step. But none of them allows to specify exactly the price ranges you want to see.

Another point is that Magento subtracts 0.01 to the highest value of each price range when displaying them. I.e. if range is "100-200", Magento will display "100.00 - 199.99".

This extension allows you to set the exact price ranges you need and to disable subtraction of 0.01.

## Compatibility
Original version tested on Magento CE 1.6.2.0 and 1.7.0.2
Forked version tested on Magento CE 1.5.1.0

## Notes
* Free and open source
* Fully configurable
* Bundled with English and French translations

## Installation
Just download the "app" folder and paste it into the root directory of your Magento application. It will be merged with the existing "app" folder.

No Magento files will be modified but class "Mage_Catalog_Model_Layer_Filter_Price" will be extended.

## Usage
In __System > Configuration > Catalog > Catalog > Layered Navigation__, this extension adds two new options: __Price Ranges__ and __Subtract 0.01 from the highest value of each price range__

![](http://4.bp.blogspot.com/-ubCE1QQ-XSs/UHkh7AbIvBI/AAAAAAAALMg/dACSlC0T6Xw/s1600/price-ranges.png)

This option is only available if you choose "Manual" for "Price Navigation Step Calculation".

Note : on the screenshot you see a ";" at the end of the field. This is just because the value continues on the right, this is not the last character.

You have to stick to this format:
* ; separates prices ranges
* - separates min and max values of a given range
* min value of the first range and max value of the last range are optional. Magento will respectively display "Under [max1]" and "[minN] and above".

Leaving this field empty means stay with the Magento basic behavior for manual calculation.

![](http://1.bp.blogspot.com/-IySUPzoaAls/UHkijgjwwPI/AAAAAAAALMo/f0oaG3zQzKo/s1600/substract-001.png)

This option is available regardless of the value you choose for "Price Navigation Step Calculation".
* Select "Yes" to stay with the Magento basic behavior
* Select "No" to disable subtraction of 0.01

## Changelog
### 1.0
* initial release
