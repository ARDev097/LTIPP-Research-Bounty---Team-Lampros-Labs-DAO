# Sector Growth, User Interaction, and Incentive Effectiveness Dataset

## Overview
This dataset has been compiled to analyze sector growth, user interaction, and incentive effectiveness within the Arbitrum ecosystem, particularly focusing on the protocols participating in the Long-Term Incentive Pilot Program (LTIPP). The analysis spans from March 4, 2024, to September 2, 2024, with a specific focus on the LTIPP incentive period from June 3, 2024, to September 2, 2024, and a pre-incentive interval of equivalent duration for comparative analysis.

## Dataset Structure
The dataset is organized into separate folders for each protocol that received grants in the LTIPP. Inside each protocol's folder, there is a sub-folder containing the transactions data with the following columns:

- **block_time**: The timestamp when the transaction was executed.
- **user**: The address of the user who performed the transaction.

### Example Directory Structure

- Protocol A/
    - Protocol A Transactions.csv

- Protocol B/
    - Protocol B Transactions.csv


## Description of Dataset

### Columns

- **block_time**:
  - Type: DateTime
  - Description: The exact time when the transaction was executed on the blockchain.
- **user**:
  - Type: String
  - Description: The blockchain address of the user who performed the transaction.

### Data Collection Periods

- **Pre-Incentive Interval**: March 4, 2024, to June 3, 2024
- **Incentive Program Period**: June 3, 2024, to September 2, 2024

### Data Source

The data was collected using queries on Dune Analytics, focusing on transactions made by users of each protocol using the protocol's contract address and the available tables on the Dune Analytics platform.

## Steps of Data Collection

1. **Dividing Protocols into Sectors**: 
   - Protocols were categorized into sectors such as DeFi, Gaming, Oracles, etc., to facilitate sector-wise analysis.

2. **Finding Relevant Tables on Dune Analytics**: 
   - Tables available on Dune Analytics were identified for collecting transaction data.

3. **Identifying Contract Addresses**: 
   - Contract addresses for each protocol were located to trace transactional data accurately.

4. **Writing Queries**: 
   - SQL queries were constructed and executed on Dune Analytics to collect the necessary columns ('block_time' and 'user') and filter the data by the specified time duration.

## Metrics for Analysis

1. **Daily Active Users (DAU)**: 
   - The number of unique users performing transactions each day.

2. **Monthly Active Users (MAU)**: 
   - The number of unique users performing transactions each month.

3. **Transaction Count**: 
   - The total number of transactions performed by each user.

4. **User Retention Rates**: 
   - The proportion of users who continue to perform transactions from one period to the next.

## Objective

The primary objective of this dataset is to:

- Identify which sectors (e.g., DeFi, gaming) witnessed the largest growth in user activity and user base during the incentive programs.
- Analyze user retention rates and interaction patterns within each sector, categorizing actions as reward-driven or genuine long-term usage.
- Evaluate different ways incentives are utilized across the Arbitrum ecosystem and their effectiveness in creating sticky liquidity and long-term user engagement.

## Usage

Researchers and analysts can use this dataset to:

- Conduct in-depth investigations into the effectiveness of LTIPP for participating protocols.
- Evaluate the growth and engagement within various sectors of the Arbitrum ecosystem.
- Analyze the impact of incentive programs on user behavior and transaction patterns.
