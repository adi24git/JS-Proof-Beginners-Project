# JS-Proof-Beginners-Project
/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

// create a variable to hold your NFT's
let n0fNFTs = 0; 
/* this function will take in some values as parameters, create an
   NFT object using the parameters passed to it for its metadata, 
   and store it in the variable above.
*/
function mintNFT (name,id,phonenumber) {
 const nft = {
 name,
 id,
 phonenumber
};
n0fNFTs++;
 return nft;
} 
// Create an array to hold the minted NFTs
let nftArr = [];
// Create an NFT and store it in the array
let firstNFT = mintNFT("Aditya Pratap Singh","12345","9898898988");
nftArr.push(firstNFT);
// Create another NFT and store it in the array
let secondNFT = mintNFT("Abhijeet Singh","12348","8787787867");
nftArr.push(secondNFT);
// Create another NFT and store it in the array
let thirdNFT = mintNFT("Sujay Biswas","12349","1212323212");
nftArr.push(thirdNFT);
// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs () {
 for(let i=0; i <nftArr.length; i++) {
  let nft = nftArr[i];
  console.log("Name: " + nft.name);
  console.log("ID: " + nft.id);
  console.log("Phonenumber: " + nft.phonenumber);
  console.log("________________");
} 
}
// print the total number of NFTs we have minted to the console
function getTotalSupply() {
 console.log("Total number of NFTs: " + n0fNFTs);
}
// call your functions below this line
// print the list of NFTs
listNFTs();
// print the total supply
getTotalSupply();
