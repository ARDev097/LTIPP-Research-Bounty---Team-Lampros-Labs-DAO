# User Actions with ARB Rewards and Unintended Incentivized Actions

## Overview
This dataset has been compiled to investigate how users utilize ARB rewards received from various protocols and their subsequent actions. It aims to track the flow of ARB rewards, categorize actions such as selling, reinvesting, or adding to liquidity pools, and analyze behavior by protocol cohorts. The dataset also focuses on identifying any unintended incentivized actions resulting from the current incentive programs and proposing adjustments to mitigate such behaviors.

## Dataset Structure
The dataset is organized into two parts:

1. **ARB Reward Recipients**: 
   - Contains transaction records from various protocols where the "from" addresses are the reward distributor addresses and the "to" addresses are the ARB reward recipients.
   - Includes columns for transaction hash, transaction time, and the amount of ARB tokens involved.

2. **Subsequent Transactions of Recipients**: 
   - Includes transaction records where the "from" addresses are the recipients' addresses, and the "to" addresses indicate where the ARB tokens are being spent or transferred.

### Example Directory Structure

- Protocol A/
    - Protocol A - ARB Reward Recipients.csv
    - Protocol A - ARB Reward Utilization.csv

- Protocol B/
    - Protocol B - ARB Reward Recipients.csv
    - Protocol B - ARB Reward Utilization.csv

## Description of Dataset

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

## Data Source
The data was collected using queries on Dune Analytics. The process involved:
1. **Identifying ARB Reward Distributing Addresses**: Tracking token flow on Arbiscan and verifying distributor addresses from the ARBgrant website.
2. **Writing Queries for Reward Distribution**: Using distributor addresses and Dune Analytics tables to collect transaction data of ARB reward recipients.
3. **Writing Queries for Subsequent Transactions**: Collecting data on subsequent transactions of ARB tokens using recipient addresses and Dune Analytics tables.

## Metrics for Analysis

- **Token Flow Tracking**: Analyzing how ARB tokens are transferred and spent by reward recipients.
- **Categorization of Actions**: Identifying actions such as selling, reinvesting, or adding to liquidity pools.
- **Behavior Analysis by Protocol Cohorts**: Examining user behavior patterns within different protocol groups.
- **Unintended Incentivized Actions**: Identifying and proposing adjustments for unintended actions resulting from the incentive programs.

## Objective
The primary objectives of this dataset are to:
- Investigate how ARB rewards are utilized and track subsequent user actions.
- Analyze the behavior of reward recipients and categorize their actions.
- Identify any unintended incentivized actions and propose potential improvements to the incentive programs.

## Usage
Researchers and analysts can use this dataset to:
- Examine the utilization of ARB rewards and understand user behavior.
- Evaluate the effectiveness of incentive programs and identify unintended consequences.
- Propose improvements to optimize incentive program design and user engagement.
