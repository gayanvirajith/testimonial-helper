# Testimonial Helper #

## Overview ##

This module will create templates and fields which are related to functioning testimonial feature. Idea of this module is simply saving time without creating fields and templates when it comes to usage.

### How to install ###

1. Copy the files for this module to /site/modules/TestimonialHelper/
2. In admin: Modules > Check for new modules. 
3. Click *install* for the Testimonial Helper. 
4. Create relevant templates under /sites/templates. eg: testimonials.php

### How to use ###

1. In admin: Pages > New > Select template as `testimonial-single` > Save
2. Create Children pages as per your choise.

### How to use api ###

To get a markup version of all testimonials, use following:
````
<?php if($modules->isInstalled("TestimonialHelper")): ?>
<?php echo $modules->get('TestimonialHelper')->getCustomerExperienceSideBarSummaryTiles() ?>
<?php endif; ?>
````
To get a page array use following:
````
<?php if($modules->isInstalled("TestimonialHelper")): ?>
<?php $items = $modules->get('TestimonialHelper')->getAllTestimonials() ?>
<?php endif; ?>
````
Page array and pagination:
````
<?php if($modules->isInstalled("TestimonialHelper")): ?>
<?php $items = $modules->get('TestimonialHelper')->getAllTestimonials(); ?>
<?php foreach($items as $item): ?>
<?php // info as you wish ?>
<?php endforeach; ?>
<?php $pager = $modules->get('TestimonialHelper')->renderPagination($items); ?>
<?php echo $pager; ?>
<?php endif; ?>
````


