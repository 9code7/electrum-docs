.. _coldstorage:

Cold Storage
============

This document shows how to create an offline wallet that
holds your Bitcoins and a watching-only online wallet that
is used to view its history and to create transactions that
have to be signed with the offline wallet before being
broadcast on the online one.


Create an offline wallet
------------------------

Create a wallet on an offline machine, as per the usual process (file
-> new) etc.

After creating the wallet, go to Wallet -> Information.

The Master Public Key of your wallet is the string shown in this popup
window.  Transfer that key to your online machine somehow.


Create a watching-only version of your wallet
---------------------------------------------

On your online machine, open up Electrum and select File ->
New/Restore. Enter a name for the wallet and select "Standard wallet".

Select "Use a master key"

Paste your master public key in the box.

Click Next to complete the creation of your wallet. 
When you're done, you should see a popup informing you that you are opening a watching-only wallet.

Then you should see the transaction history of your cold wallet.

Create an unsigned transaction
------------------------------

Go to the "send" tab on your online watching-only wallet,
input the transaction data and click "Pay". 

Click "Advanced", then click "Finalize", then click "Export" and choose the "Export to file" option. 
This will save the transaction file to a location on your computer which you specify. Close the
window and transfer the transaction file to your offline
machine (e.g. with a usb stick).

Get your transaction signed
---------------------------

Transfer the transaction file you created from the step above to your 
offline computer. Then, select Tools -> Load transaction -> From file
in the menu and select the transaction file you just transferred. 

Click "sign". Once the transaction is signed, the Transaction ID
appears in its designated field.

Click save, then click "Export" and choose the "Export to file" option. This will 
create a signed transaction file which you will need to transfer to your 
online watching-only wallet. 

Broadcast your transaction
--------------------------

On your online machine, select Tools -> Load transaction -> From File
from the menu. Select the signed transaction file. In the window that
opens up, click "Broadcast". The transaction will be broadcasted over
the Bitcoin network.

