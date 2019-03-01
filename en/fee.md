# Ontdex Fee Note


Ontdex is the first de-centralized exchange on ontology. It supports ONT/ONG, OEP4-token/ONG, OEP5-token/ONG and OEP8-token/ONG as trading pair.

If there are stable currencies on ontology that meet the OEP4 standard, ontdex will also support trading pairs with stable currencies as quoted currencies.
So you can see OEP4-token/OEP4-token trading pair.



In view of the particularity of decentralized exchanges and the decimals of ONT, ontdex will use the quoted currency as the handling fee for each trading pair. The specific rules and handling fee rates are as follows:



1. The current handling fee rate of ontdex is two thousandths, and both buyers and sellers have to pay it.



2. Sellers have to pay two thousandths of the total transaction as handling fees. For example, ONT/ONG trading pairs sell 10 ONTs at a price of 1.0, and the total transaction amount is 10 ONG. At this time, they have to pay 0.02 handling fees, so the actual number of ONG purchased is 9.98.



3. The buyer of the transaction has to pay two thousandths of the total transaction as the handling fee, which will be transferred to ontdex smart contract in advance and paid at the time of the transaction; if the user cancel the order, the handling fee will be returned together;
For example: ONT/ONG transaction pair, if the user places a order with a price of 1.0 and a quantity of 10 ONT, the total transaction amount is 10 ONG. When the user orders, he will transfer 10 ONG to the contract for transaction, and 0.02 ONG will be transferred to the contract as the prepaid handling fee. When the order is completed, the user will receive 5 ONT, and the prepaid service fee will deduct 0.01ONG. At this time, the user withdraws the order. The user's account will receive the remaining 5 ONGs that are not traded and 0.01 ONGs that are not consumed.



4. Order-placing restriction: Because of the handling fee on the chain, ontdex limits the minimum transaction amount of each order. When the current order amount is less than this value, the user will not be able to place the order successfully, and the current minimum transaction amount is limited to 10ONG.
