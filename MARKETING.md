# ManyVolumeSignalMonster

## What is it?

## TL;DR

We hacked the combined, averaged trends in volume among many exchanges to predict changes in price on a given target exchange... in our case: BitMEX, which allows as much as 100x leverage on some trading pairs. 

## Long-form

An automated trading bot taking some work another party has made open-source, and building onto it a signal execution strategy. The original work is live at https://aggr.trade and is available at https://github.com/Tucsky/SignificantTrades


Simply put, it aggregates actual trades that happen across (as many as) 16 cryptocurrency exchanges. Wait! Before I lose you! The natural ups and downs that exist with crypto (all of them (save for some exceptions) much like Bitcoin, which is sometimes $9000 in the morning when you use it to buy a laptop then $12000 later that day - or the opposite direction!) leave different exchanges with sometimes very different opinions about the price of a given trading pair. What this means for us savvy traders is that we can spot trends across many exchanges sporting much (combined in a useful graph, with handy indicators...) volume among them - before these trends are realized on their competing exchanges. Try it yourself - load https://aggr.trade and voila, along the bottom graph you'll see green and red bars (meaning buy/sell volume) and a yellow line and a red line - in the above graph, you'll see that the average price among all of the exchanges in use will tend to go up after the yellow line (which is the trend of the buying volume over the last 14 volume bars) crosses above the red line, and then the price will follow downwards along with the red line crossing above the yellow line... 


Enter my friend @crypto_tra who recommended to me I look into a way to hack this awfully apparent set of trends. After some mcgivering and a lot of trial and error - learning from mistakes - we finally have a stable version to market!


## Want a more technical explaination?


Feel free to visit the placeholder Github README file for a deep-dive into the logic, failsafes, and additional details: https://github.com/DunnCreativeSS/ManyVolumeSignalMonster


## Word to the wise


10% Tier-1, 5% Tier-2 affiliate commissions on contributions or subscriptions - as a fraction of total weighted value, which means recurring revenues :) :) Here's what I mean: https://docs.google.com/spreadsheets/d/1qUSILqCyizkqF-p5k_6ovuSWNsmtfofD77u4tSTq_Ds/edit?usp=sharing - notice Free Lunch Lady? She didn't contribute a dime but she's earned a steady stream of income through affiliate marketing :D


## Want to earn MoAr???!?


1. It's like an open-ended bounty campaign...
2. Can you do a service?
3. Can you add value?
4. Social media, blogs, email marketing, PPC, or any kind of qualified traffic from marketing will do the trick!
5. Anyone who contributes any amount of work more than just referring friends & family will earn a % additional 1-Tier and 2-Tier commissions scaling according to cost-effort!


## People can share the riches!

CONTRIBUTION FUND: 3BMEXpTrCRmV55ziRjTMu4zMGCU1UrbUbi

1. Send me TX, I'll keep track of who has how much %
2. I'll take 30% of realized profits weekly, the other 70% goes back to contributors weekly
3. If you refer someone else and they supply your TG handle to me or admins, you'll get 10% of their contribution added to your weight - and 5% for their referrals in Tier-2
4. The weights work like this example: https://docs.google.com/spreadsheets/d/1qUSILqCyizkqF-p5k_6ovuSWNsmtfofD77u4tSTq_Ds/edit?usp=sharing


## For people that don't like sharing?

1. People can subscribe to use the bot using their own livenet API keys (and they can test on testnet with fake money for free!)
2. Cost is about $50 upfront + $50 recurring monthly minimum cost, and 5% of their realized gains settled monthly.
3. People that refer subscribers get 10% of upfront and recurring income, + 5% Tier-2, which is calculated and added to the total weight of everyone whos in the contribution fund, creating evergreen wealth (check above Google Sheet)

## Telegram!

join our growing community! https://t.me/ManyVolumeSignalMonster