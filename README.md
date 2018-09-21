
## You Need a Web 3.0 Enabled Browser

The What Does Nadia Think?™ platform requires a Web 3.0 enabled browser. You can enable Web 3.0 support on Chrome, Firefox, or Brave Browser with the MetaMask extension, or you may use standalone browsers like Mist and Parity. You can also use the Cipher iOS app to play on your iPhone.  
  
Think of Web 3.0 as having decentralized Facebook account where you can login to every site with, and where you always decide what data you share with other people. MetaMask now has Trezor hardware wallet support, which means that it is possible to keep your Ether safe, even if your computer has every trojan in the world on it. It's like an RSA token you got for your bank account, but far more secure.  

## You Need Ether

If you don't have Ether, then you are out of luck, because you need to use all decentralized applications, or Dapps. Ether is the currency that allows smart contracts to exist immutably. You pay miners gas with each transaction to guarantee the integrity of the network, and you use Ether to buy things, or better yet, play stupid games like What Does Nadia Think?™.  

## Selecting Your Answer

Each market is a separate smart contract managing everything for that particular quiz. Each quiz will have exactly four possible answers. It's as simple as clicking on an answer to select. Once you make a selection, it turns green, while the betting amount slider and bet button become enabled.  
  
Don't worry, you can still change your answer. Your Ether is not taken until you explicitly send it, along with the data that tells the contract what selection you made. All of this could be done on the command line, but thanks to Web 3.0, the frontend is designed in a way to make it a familiar clickable experience.  

## Selecting Your Bet

It's as simple as dragging the slider. Keep in mind that each market is parimutuel, meaning that you will split the entire pool proportionally with the rest of the people who selected correctly. This means that there is no advantage to betting a large amount on an answer that nobody has selected yet, because you can win the entire pool with a bet of only 1 Wei.  
  
You may notice that the slider only goes from 0.01 to 1 Ether. So how could you bet only 1 Wei. This slider is for convenience and not an absolute limit. If you are more advanced, you may transact manually with the contract and send any amount.  
  
You should also be aware that it will cost you Ether to pay for the gas of both placing your bet, and claiming your winnings. Therefore, it doesn't make sense to bet too small.  

## Wait for the Quiz to Close

Each quiz has a countdown and automatically closes after a specified time period. Once the contract is closed, the contract exists in a state of limbo until an administrator (the contract creator) manually adds the answer, and links to the verification source. All answers (can be in the form of audio, an image, or text) are hashed with SHA256 and stored securely locally until the answer is revealed by the contract creator.  
  
You cannot reverse a hash to find the answer, you can only take the verification hash and match it to the immutably added hash in the contract by running the SHA256 yourself. An image or audio file is much larger that a simple hash, and you can't zoom in and enhance from just a hash. With text verification files, they are salted as to stop people from simply running the SHA256 four times on all of the answer.  
  
In rare cases a contract might be voided. This could happen by a set timeout period after closure if an administrator doesn't post the answer to the contract, or in the case of a manual void. Please refer to the rules for more info on this.  
  
If you've selected correctly the answer, and the administrator has published the result, then you can proceed to claim your winnings.

## Claim Your Winnings

Winnings are not sent automatically to you. You must transact with the contract via the "Claim Winnings" function to get your winnings. There is no time limit to do this, so if the network is congested, it makes sense to wait so you can make this transaction for a minimum gas price.  
  
You can think of the "Claim Winnings" function as asking a teller to send you your money. It's a message without any Ether being attached, but it unfortunately does cost you gas due to the way things work currently in Ethereum. Some day it might be possible for a contract to automatically to do this.

## What Happens if Nobody Selects the Correct Answer

No integrity fee is taken, and all Ether is refunded. You will need to manually ask for a refund by transacting with refund() and including the integer of your answer. If you chose Answer 1, then you would pass through the integer 0 to the contract as all arrays in Solidity start from 0. This differs from the process of win you chose the winning answer because the contract does not anticipate refund situations occurring very often. The additional complexity to make it a one click operation is not worth the increased gas costs.
  

## Sigh, I've Actually Lost – Now What?

Nothing. You've lost. The winners have collected your Ether. The only thing you can possibly do is rage about your loss in the comments and tell strangers on the street what an incompetent quizzer you are.  
  
Better luck next time!
