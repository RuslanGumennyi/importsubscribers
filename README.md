# Magento Import Subscribers module
--------------------------

## Description

This simple extension allows to import a list of subscribers.
Currently supported file formats: 
- txt (only list of emails, one per line),
- csv ('Email' is required field, other can be omitted) 
- Excel XML (same as csv)  
 
Order of the columns can be anything, but it's important to pass correct headings, for example: 'Email' (not 'email'), 'Store View', 'Status', etc. 
 
Valid column names (any other will be ignored):
- Email - email addresses.
- Type  - can be Customer or Guest. IMPORTANT: If the Type specified as Customer, but the client with such e-mail doesn't exist, it will be saved as Guest.
- Status - One of Subscribed, Unsubscribed, Not Activated, Unconfirmed.  
- Store View - name of your site's store view in which you want insert subscribers list (must be created prior to proccess, otherwise default will be used ). 

If count of rows in your file more than 50-60 thousands, it'd be better split it for smaller parts.
IMPORTANT: It doesn't care of duplicates, so one should remove them manualy prior to import.       

## Requirements
- Magento Community Edition v1.6
- PHP >= 5.2

## License

Copyright (c) 2011 Ruslan Gumennyi. Licensed under the [MIT License](http://en.wikipedia.org/wiki/MIT_License).
