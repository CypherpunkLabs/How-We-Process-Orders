# How-We-Process-Orders

We are a transparent company who truly follows a new paradigm, KYCNYC - Know Your Company, Not Your Customer. We believe this to the core and in 
ever aspect we work to follow this model to protect everyone. 

This walkthrough documentation is to provide insight as to how we currently process payments and execute order fulfillment in a privacy focused way.

As we have no user data as we do not even run a database it is important to keep in mind that PayPal does have a record and that there is a record
of orders on the blockchain that you may have paid through. However, we have no record store or data. This is imperative to how we operate. We
care about your privacy and while we love you supporting us we do not want to know you so we can protect your privacy. 


# Compliance

Compliance is a complicated and fickle manner, we will always comply with law enforcement as we have no data or correclation with the customers to the order.
By operating in this fashion we can comply without risk to you. This allows for a better way of operation as well as protective measures for all parties involved.
Our canary will be live soon with our keys and verification process of notifications if we recieve an inquiry. We do this for transparency.

# Our Backend

We do plan to open source 99% of our backend services over time. Originally these were created with minimum features. The only code we will not be open sourcing
will be our API keys to providers and such. So you would be able to facilitate running your own operation with our tooling. We find this important so that the 
ideas and processes could be used for other software services. We value healthy competition as well as support innovative takes on existing ideas. We are also
a promoter of FOSS(Free and open-source software). You should expect to see some of this code to be available soon as we refine it and make it better for general use, as it sits right now some changes
are being made to make it much more flexible with other providers. We are also going to distribute some Rust libraries to include in your own projects for the future. 

Our backend is 100% Rust.


# PayPal

Using PayPal has some inherit risks in and of itself but those risks are isolated to them. We provide only digital goods/services so at no point do we require shipping
information or further details from the user. PayPal obviously does have this data and that is important to understand as they could provide information if they are 
requested by law enforcement. We do not have such data and simply use their API to request details. Our API check runs once a minute. 

https://developer.paypal.com/docs/api/orders/v2/#orders_get

We only request order type, duration, and region(coming soon to the site).

As we do not offer refunds in anyway it is important to understand that we do not have access to the console for PayPal. We run a process every day at 4:30pm Central Time
to send any PayPal order money received to the company bank. We do this for consistency and auditing on our end with all cryptocurrency payments too. As we are a transparent
company we wanted to disclose this information about PayPal so that you are aware of how we operate with them as a payment option. Their button is their button, their option 
to use the credit card at checkout is also only their's. We do not have a way to store data nor do we want to. 

Our website code will be made open source with a few things scrubbed out like keys used to call PayPal API for order submission. This process is the same as any other site you 
have used with purchasing with PayPal. 


# Bitcoin

Our payment address are available through the KYC(LOL) repo: https://github.com/CypherpunkLabs/KYC-Know-Your-Company-. We run a number of tools i wrote years ago that
simply checks each address and transaction, verifies that it has the corresponding confirmations(6 now, not 20), and then executes to deliver the corresponding type,
duration, and region(available on site soon). This simply is a way of managing each item as if it were a SKU. Please refer to the KYC repo to check when wallets change
based on SKU updates. Since we have no database or any data, this way the backend software can run the necessary instructions. 

We encourage you to use mixed coins, preferrably with Whirlpool by Samourai Wallet to prevent transaction from being peeled and privacy compromised. We believe in good
privacy tools and as new ones may pop up, as long as they are held to same standard of protections of the user we will promote their use. We want everyone to use the right
tools for them, however, we must encourage you to do your research and understand the attack vectors with each. 

Every day at 4:30pm Central Time we execute a sending of coins to Coinbase for time being. Our providers are not yet accepting bitcoin but we are changing that and once
they do we will be completely circular on this front. Our goal is to keep it peer to peer with Bitcoin. At this time we do have to convert to fiat for costs of infrastructure
but as the aforementioned providers begin to accept we will be changing this model. We will update this repository once it is done. 


# XMR (Coming Soon)

