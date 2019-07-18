# ManyVolumeSignalMonster

## Telegram!

join our growing community! https://t.me/makemarketsgeneratecrypto

## What is it?

https://aggr.trade https://github.com/Tucsky/SignificantTrades reimagined to use buy/sell signals in automated trades!


Supporting BitMEX for now on livenet+testnet, with more exchanges tbd...


This repo exists to provide a 'sponsor' link (should I get approved for the beta...) while the livenet and testnet code are now both private.


## Word to the wise


10% Tier-1, 5% Tier-2 affiliate commissions on contributions or subscriptions - as a fraction of total weighted value, which means recurring revenues :) :) Here's what I mean: https://docs.google.com/spreadsheets/d/1qUSILqCyizkqF-p5k_6ovuSWNsmtfofD77u4tSTq_Ds/edit?usp=sharing - notice Free Lunch Lady? She didn't contribute a dime but she's earned a steady stream of income through affiliate marketing :D


## Want to earn MoAr???!?


1. It's like an open-ended bounty campaign...
2. Can you do a service?
3. Can you add value?
4. Social media, blogs, email marketing, PPC, or any kind of qualified traffic from marketing will do the trick!
5. Anyone who contributes any amount of work more than just referring friends & family will earn a % additional 1-Tier and 2-Tier commissions scaling according to cost-effort!


## Share the riches!

CONTRIBUTION FUND: 3BMEXpTrCRmV55ziRjTMu4zMGCU1UrbUbi

1. Send me TX, I'll keep track of who has how much %
2. I'll take 30% of realized profits weekly, the other 70% goes back to contributors weekly
3. If you refer someone else and they supply your TG handle to me or admins, you'll get 10% of their contribution added to your weight - and 5% Tier-2
4. sample weights: https://docs.google.com/spreadsheets/d/1qUSILqCyizkqF-p5k_6ovuSWNsmtfofD77u4tSTq_Ds/edit?usp=sharing
5. it'd be fun to put this into a tradeable token so people can buy/sell stake?



## Does it perform?

For anyone who's interested in such things, my crypto trading bot has seen some huge improvements suggested by our small community.. as of just over 1/2 of a day ago when I added configurable % take profit and configurable % stop loss, after my friend with his $30 on livenet got liquidated and he suggested more failsafes... also waiting for 3 10-second (by default) bars to confirm a signal to buy/sell... learning curves :)



Testnet #1 balance since 1/4 of a day ago is:



gains (margin): 184 %



gains (wallet): 213 %



Testnet #2 balance since 1/2 of a day ago is:



gains (margin): 12.9 %



gains (wallet): 32.9 %



Note that the second testnet account is using the UI configurable default 'order multiplier' of 1, while my testnet is using 3x that, amplifying gains :)



I've added whitelisting of API keys or account #s so it's now ready to sell :) 


## Not a fan of BitMEX?


More exchanges to come, tbd! I'm available for bribes to fork into your favorite exchanges :)


## Get me into Github Sponsors Beta 


Your reward? % saved on subscriptions, % bonus to crowdfund contributions AND double referral income!


1. fill out this form: https://docs.google.com/forms/d/e/1FAIpQLSdE8nL7U-d7CBTWp9X7XOoezQD06wCzCAS9VpoUW6lJ03KU7w/viewform
2. you don't need to provide a github profile or email
3. for 'Which developers would you like to sponsor through GitHub Sponsors?' set github.com/dunncreativess
4. for 'anything else we should know' let them know about my efforts as dev for these bots? Tireless, sleepless nights to optimize and include feedback? :)
5. Also recommend me to participate in the limited beta. Send an email to opensource@github.com with a link to https://github.com/dunncreativess and my contact information: Telegram @RegTheIII Medium @jarettrsdunn email jarettrsdunn+git@gmail.com


### They're doubling people's sponsorships for the first year, up to $5k... 

anyone that wants to pay for the bot using GitHub (paypal or credit card) will get a 25% discount on subs, 25% bonus to their contribution's weight AND double referral % weight!

### Check it out 

I'm nearly-not-quite-able to be sponsored on GitHub! https://imgur.com/a/nLs3XBu

## If you prefer running with your own $BTC on livenet

There's a 0.005 BTC upfront + 0.005 BTC monthly charge, and 5% of your realized gains (monthly)... 


Testnet access is free :) just ask for your apikey or account # to be included in the validity spreadsheet. 


Code for live / test is available on request for audits


0. provide me with your API key for livenet/testnet, I'll add it to the valid keys spreadsheet (bots running without a valid key won't make any POST requests...like place orders)
1. if livenet, get an ADDITIONAL 10% discount on fees: https://www.bitmex.com/register/30KY2F - stop loss + take profit orders will earn me affiliate income...
2. run chromium-browser --disable-web-security --user-data-dir=~/ or google-chrome --disable-web-security --user-data-dir=~/ - Windows and Mac directions: https://www.codevoila.com/post/75/how-to-disable-same-origin-policy-in-chrome
3. http://35.239.130.201/ testnet
4. http://34.68.94.126/ livenet
5. 'couldn't load history' is a-ok
6. in settings, set trailstop+stoploss+takeprofit %s
7. in settings, set keys (be sure to tab / click off so they save)
8. in settings on one tab, set BTCUSD
9. in other, ETHUSD
10. any of the U19 pairs will also work, I need to remind myself to grab the current futures contract in a future release...
11. For both, click ON all the extra exchanges - and OFF BitMEX (it doesn't like too many websocket requests, it'll '429 too many requests' you if you reload the page too too much then '403 forbidden' ban you for an hour or two...)
12. wait 14 10s intervals for volume SMAs
13. check dev tools console for errors (change log level, turn off info/debug)
14. after SMAs cross, it'll enter a buy/sell - and if the orders fill then trailstop+takeprofit+stoploss
15. check performance of all bots here: http://35.239.130.201:3000/
16. you can lessen short-term sensitivity two ways: 1. increase timeframe (from 10s) 2. increase SMA length (from 14)

## @crypto_tra gets free lifetime subscription 

First for pointing out strategy, then I forgot and gave him another free lifetime sub for being the first person other than me to test on livenet :) so he naturally gets additional referral commissions

## Bot does a bunch of smart things:

1. if - pos, it doubles buys
2. if + pos, it doubles sells
3. Original buy/sells are POST-ONLY limits, takeprofit and stoploss are MARKET but you can configure their respective %s
4. up/down to match price tickSize
5. price is a function of avail margin, which is then multiplied by configurable 'ordermult'
6. except when avail margin < 17.5% (will later be a configurable variable), then it stops buying in current pos direction
7. it'll miss out some of the orders, ensuring it stays pos/neg on longer swings - fun fact there's an unused 'testingtesting123' variable that could be made into a configurable one that enters the original limit orders at the opposite of bid/ask for buy/sell, which fills orders much much quicker at the expense of fees...

# join our growing community! https://t.me/makemarketsgeneratecrypto