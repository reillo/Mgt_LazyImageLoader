Mgt Lazy Image Loader For Magento
====================================

## FEATURES
-----------------

There are many ways to improve the performance of your magento store. 
All shop owners will know that product images play an important part. 
However, there is one problem with this. 
The more images you have, the slower the site loads and utilizes more bandwidth. 
A very good solution to this is to load your images on demand, or what is most commonly known as lazy loading.

Conclusion
Lazy loading is a additional way to improve the page's loading time and overall performance. 
You only need 1-2 minutes to install this magento extension.

## INSTALLATION
-----------------

1. Extract zip archive and copy contents to the app/folder of your Magento installation
2. Open the file "app/design/frontend/default/default/catalog/product/list.phtml"

 <pre>
<code>
 search for
  <img src="<?php echo $this->helper('catalog/image')->init($_product, 'small_image')->resize(135); ?>"
 width="135" height="135" alt="<?php echo $this->stripTags($this->getImageLabel($_product,      'small_image'), null, true) ?>" />
</code>
</pre>


<pre>
<code>
replace with
<img class="lazy" src="<?php echo $this->getSkinUrl('images/mgt_lazy_image_loader/loader.gif'); ?>" data-src="<?php echo $this->helper('catalog/image')->init($_product, 'small_image')->resize(135); ?>" width="135" height="135" alt="<?php echo $this->stripTags($this->getImageLabel($_product, 'small_image'), null, true) ?>" />
  </cody>
</pre>
    
3. Clear the cache in Admin > System > Cache Management