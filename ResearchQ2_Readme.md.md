# User Actions with ARB Rewards and Unintended Incentivized Actions Dataset 🎯

## Overview 🌟
This dataset has been compiled to investigate how users utilize ARB rewards received from various protocols and their subsequent actions. It aims to track the flow of ARB rewards, categorize actions such as selling, reinvesting, or adding to liquidity pools, and analyze behavior by protocol cohorts. The dataset also focuses on identifying any unintended incentivized actions resulting from the current incentive programs and proposing adjustments to mitigate such behaviors. The current dataset contains data up to the latest date, and the remaining data will be updated by the end of September. Additionally, the dataset contains a limited number of columns from Dune as these are the necessary data points for our analysis.

## Dataset Structure 🗂️
The dataset is organized into two parts:

1. **ARB Reward Recipients**: 
   - Contains transaction records from various protocols where the "from" addresses are the reward distributor addresses and the "to" addresses are the ARB reward recipients.
   - Includes columns for transaction hash, transaction time, and the amount of ARB tokens involved.

2. **Subsequent Transactions of Recipients**: 
   - Includes transaction records where the "from" addresses are the recipients' addresses, and the "to" addresses indicate where the ARB tokens are being spent or transferred.

### Example Directory Structure 📁

- **Protocol A/**
    - `Protocol A - ARB Reward Recipients.csv`
    - `Protocol A - ARB Reward Utilization.csv`

- **Protocol B/**
    - `Protocol B - ARB Reward Recipients.csv`
    - `Protocol B - ARB Reward Utilization.csv`

## Description of Dataset 📝

### Columns

#### ARB Reward Recipients

- **transaction_hash**:
  - Type: String
  - Description: Unique identifier for each transaction.

- **transaction_time**:
  - Type: DateTime
  - Description: Timestamp when the transaction occurred.

- **from_address**:
  - Type: String
  - Description: Address from which the ARB tokens were distributed.

- **to_address**:
  - Type: String
  - Description: Address receiving the ARB tokens.

- **amount**:
  - Type: Float
  - Description: Amount of ARB tokens involved in the transaction.

#### Subsequent Transactions

- **transaction_hash**:
  - Type: String
  - Description: Unique identifier for each transaction.

- **transaction_time**:
  - Type: DateTime
  - Description: Timestamp when the transaction occurred.

- **from_address**:
  - Type: String
  - Description: Address from which the ARB tokens were spent or transferred.

- **to_address**:
  - Type: String
  - Description: Address receiving the ARB tokens.

- **amount**:
  - Type: Float
  - Description: Amount of ARB tokens involved in the transaction.

## Data Source 🔍

The data was collected using queries on Dune Analytics. The process involved:

1. **Identifying ARB Reward Distributing Addresses**: 
   - **Compiled Funding Addresses**:
     - Gathered the list of funding addresses from the proposals of different protocols participating in LTIPP.
   - **Traced Arbitrum Flow**:
     - Used Arbiscan to trace the transaction flows of these funding addresses on the Arbitrum network. Looked for any addresses involved in these transactions that might be associated with distribution activities.
   - **Identified Potential Distribution Contracts**:
     - Analyzed the transaction flows to identify addresses that handle large volumes of transactions or exhibit distribution patterns. Focused on addresses that distribute funds or tokens to multiple recipients, as these are likely to be distribution contracts.
   - **Cross-Checked Addresses**:
     - Cross-referenced the potential distribution addresses with the contract addresses listed on the Arbitrum Grants website.

2. **Writing Queries for Reward Distribution**: 
   - Using the distributor addresses and relevant data tables from Dune Analytics, we collected transaction data of ARB reward recipients.

3. **Writing Queries for Further Transactions**: 
   - Using the list of recipients from the reward data and relevant tables from Dune Analytics, we collected data on further transactions of the ARB tokens.

## Metrics for Analysis 📊

- **Token Flow Tracking**: 
   - Analyzing how ARB tokens are transferred and spent by reward recipients.

- **Categorization of Actions**: 
   - Identifying actions such as selling, reinvesting, or adding to liquidity pools.

- **Behavior Analysis by Protocol Cohorts**: 
   - Examining user behavior patterns within different protocol groups.

- **Unintended Incentivized Actions**: 
   - Identifying and proposing adjustments for unintended actions resulting from the incentive programs.

## Objective 🎯

The primary objectives of this dataset are to:

- Investigate how ARB rewards are utilized and track subsequent user actions.
- Analyze the behavior of reward recipients and categorize their actions.
- Identify any unintended incentivized actions and propose potential improvements to the incentive programs.

## Usage 🔧

Researchers and analysts can use this dataset to:

- Examine the utilization of ARB rewards and understand user behavior.
- Evaluate the effectiveness of incentive programs and identify unintended consequences.
- Propose improvements to optimize incentive program design and user engagement.

## Additional Information ℹ️

For this research question, data has been collected for around 62 protocols. However, there are some protocols that have not received grants yet, some that have not started utilizing their received grants, and a few for which we are still clarifying certain details. We are currently working on the data collection for these protocols and will update the dataset shortly.

Feel free to reach out for any further questions or information!
