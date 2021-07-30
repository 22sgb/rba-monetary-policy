

# RBA Monetary Policy

This document outlines the various stages of the Reserve bank of Australia's typical implementation of traditional monetary policy to influence interest rates in the economy and thus exert some control over aggregate demand, enabling counter-cyclical macroeconomic policy as per Keynesian theory. It should be rendered on a platform like [StackEdit](https://stackedit.io) for the best experience.

## Cash Rate Target and the Policy Interest Rate Corridor

```mermaid
graph TB

D[Board decides on cash rate target based on RBA research]
E[RBA communicates its decision to the public]

A[First Tuesday of each month] --> C[RBA board meeting]
B[In emergency scenario] --> C
C --> D["Board decides to raise cash rate target (economy is expanding)"]
C --> E["Board decides to lower cash rate target (economy is contracting)"]
C --> F[Board makes no change to cash rate target]
D --> G["Sets loan and deposit rates for ES funds at ±0.25% from the cash rate respectively"]
E --> G
F --> G
G --> H[Gravitation of rates in STMM toward cash rate target in centre of loan/deposit rates]
H --> I[Interest rates charged by banks in rest of economy also update thus because banks need to maintain their profit margins]
```

Once the loan and deposit rates for ES funds have been set, banks will be unable to set their own loan rates higher than the RBA, as the borrower of course seeks the rate on the loan given to them to be as low as possible. If the RBA offers a lower rate, it will be taken. By the same principal, if the RBA offers a higher rate for a deposit, it will be taken. Thus, interest rates in the short-term money market should always be between ±0.25% of the cash rate target. Further, they will gravitate towards said target due to the contrasting pressures of borrowers looking for the lowest loan rate and depositors looking for the highest deposit rate. Thus, the RBA uses competition to keep interest rates in the short-term money market within target.

## Open Market Operations

```mermaid
graph TB

A[Demand for ES funds increases] --> B[Interest rates in STMM increase above cash rate target]
B --> C[RBA buys second-hand financial securities from banks and sells them ES funds in return]
C --> D["Supply of ES funds (STMM liquidity) has increased"]

E[Demand for ES funds decreases] --> F[Interest rates in STMM decrease below cash rate target]
F --> G[RBA sells second-hand financial securities to banks and accepts ES funds in return]
G --> H["Supply of ES funds (STMM liquidity) has decreased"]

D --> I[Interest rates return nearer to cash rate target by price mechanism]
H --> I
```

## Transmission Mechanism

Note that the first stage of transmission mechanism, by which interest rates from banks are affected by the cash rate target set by the RBA is detailed in the above section on the policy interest rate corridor. This section details the second stage of the transmission mechanism, by which interest rates affect output, aggregate demand, inflation, unemployment, etc.

```mermaid
graph TB

Up["Interest rates increase (loan and deposit rates)"]
Down["Interest rates decrease (loan and deposit rates)"]

subgraph S [Savings and Investments Channel]
	Up --> SU1[Households have greater incentive to save because higher deposit rates]
	SU1 --> SU2[Households spend less, decreasing consumption]
	SU1 --> SU3["Households have lesser incentive to borrow (higher loan rates)"]
	SU3 --> SU2
	SU2 --> ADdown
	Up --> SU4[Firms have less incentive to borrow to invest in new capital etc.]
	SU4 --> ADdown

	Down --> SD1[Households have lesser incentive to save because lower deposit rates]
	SD1 --> SD2[Households spend more, increasing consumption]
	SD1 --> SD3["Households have greater incentive to borrow (lower loan rates)"]
	SD3 --> SD2
	SD2 --> ADup
	Up --> SD4[Firms have greater incentive to borrow to invest in new capital etc.]
	SD4 --> ADup
end

ADup["AD = C + I + G + (X-M), therefore aggregate demand increases"]
ADdown["AD = C + I + G + (X-M), therefore aggregate demand decreases"]
```

```mermaid
graph TB

Up["Interest rates increase (loan and deposit rates)"]
Down["Interest rates decrease (loan and deposit rates)"]

subgraph C [Cash Flow Channel]
	Up --> CU1["Households have less disposable income (loan repayments have increased)"]
	CU1 --> CU2[Households spend less, decreasing consumption]
	CU2 --> ADdown

	Down --> CD1["Households have more disposable income (loan repayments have decreased)"]
	CD1 --> CD2[Households spend more, increasing consumption]
	CD2 --> ADup
end

ADup["AD = C + I + G + (X-M), therefore aggregate demand increases"]
ADdown["AD = C + I + G + (X-M), therefore aggregate demand decreases"]
```

```mermaid
graph TB

Up["Interest rates increase (loan and deposit rates)"]
Down["Interest rates decrease (loan and deposit rates)"]

subgraph A [Asset Prices and Wealth Channel]
	Up --> AU1["Demand for assets (e.g. housing) decreases"]
	AU1 --> AU2[Prices of assets decrease]
	AU2 --> AU3[Decrease in household wealth]
	AU3 --> AU4[Households spend less, decreasing consumption]
	AU4 --> ADdown

	Down --> AD1["Demand for assets (e.g. housing) increases"]
	AD1 --> AD2[Prices of assets increase]
	AD2 --> AD3[Increase in household wealth]
	AD3 --> AD4[Households spend more, increasing consumption]
	AD4 --> ADup
end

ADup["AD = C + I + G + (X-M), therefore aggregate demand increases"]
ADdown["AD = C + I + G + (X-M), therefore aggregate demand decreases"]
```

```mermaid
graph TB

Up["Interest rates increase (loan and deposit rates)"]
Down["Interest rates decrease (loan and deposit rates)"]

subgraph E [Exchange Rate Channel]
	Up --> E1[Interest rate differential with other global economies altered]
	Down --> E1
	
	E1 --> EU1[Global interest rates lower than Australia's]
	EU1 --> EU2["Firms have greater incentive to invest in Australia (higher returns)"]
	EU1 --> EU3[Australian dollar appreciates in value]
	EU3 --> EU4["Exports (injection) become pricier for rest of world"]
	EU3 --> EU5["Imports (leakage) become cheaper for Australia"]
	EU4 --> ADdown
	EU5 --> EU6[Inflation on imports decreases]
	EU5 --> ADdown

	E1 --> ED1[Global interest rates higher than Australia's]
	ED1 --> ED2["Firms have lesser incentive to invest in Australia (lower returns)"]
	ED1 --> ED3[Australian dollar depreciates in value]
	ED3 --> ED4["Exports (injection) become cheaper for rest of world"]
	ED3 --> ED5["Imports (leakage) become pricier for Australia"]
	ED4 --> ADup
	ED5 --> ED6[Inflation on imports increases]
	ED5 --> ADup
end

ADup["AD = C + I + G + (X-M), therefore aggregate demand increases"]
ADdown["AD = C + I + G + (X-M), therefore aggregate demand decreases"]
```

These four stages lead to one of two outcomes, that aggregate demand increases or decreases (possibly with a few extra effects along the way). This change in AD can be represented by the below diagram, which shows the aggregate demand and aggregate supply curves at their typical theoretical alignment. As per the principles of supply and demand, inflation and GDP growth (output growth) will follow logically as the equilibrium point between these two curves changes.

![AD/AS Graph](https://upload.wikimedia.org/wikipedia/commons/thumb/2/25/AS_+_AD_graph.svg/1200px-AS_+_AD_graph.svg.png)
*Image courtesy: Wikipedia (https://upload.wikimedia.org/wikipedia/commons/thumb/2/25/AS_%2B_AD_graph.svg/1200px-AS_%2B_AD_graph.svg.png)*
