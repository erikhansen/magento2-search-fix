# magento2-search-fix
Magento2 module for fixing hanging "insert to" search_tmp queries

If you'd rather apply this fix as a Composer patch, rather than installing this extension, see [this Gist](https://gist.github.com/erikhansen/a813f8cf9fe8e9836eea467bdd205659).

## tested on magento:
- 2.2.10
- 2.3.1

# Installation
## via composer
Run the following command in Magento2 root folder:
```
composer require we-are-virtua/magento2-search-fix
bin/magento setup:upgrade
bin/magento setup:di:compile
```

#FAQ
- Module does not help, what to do?

If the module does not help it means that rewrites may not work. 
You can try to remove `generated/code` directory manually and re-run 
```
bin/magento setup:upgrade
bin/magento setup:di:compile
```
or clear/flush cache
```
bin/magento cache:clear
bin/magento cache:flush
```
