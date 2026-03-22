# base-deploy-lab-
base-deploy-lab/
mkdir base-deploy-lab
cd base-deploy-lab
npm init -y
npm install --save-dev hardhat
npx hardhat
npm install dotenv @nomicfoundation/hardhat-toolbox
require("@nomicfoundation/hardhat-toolbox");
require("dotenv").config();

module.exports = {
  solidity: "0.8.20",
  networks: {
    base: {
      url: "https://mainnet.base.org",
      accounts: [process.env.PRIVATE_KEY]
    },
    baseSepolia: {
      url: "https://sepolia.base.org",
      accounts: [process.env.PRIVATE_KEY]
    }
  }
};
PRIVATE_KEY=your_private_key_here
