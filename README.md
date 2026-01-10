1. one_iv_computation: Loads SPY options data from Yahoo, takes a subset, loads into a dataframe. 
2. two_vol_surfaces: Uses the pricing data to compute implied volatility; plots surfaces and vol smiles. 
    2.5. figs ('term_structure_analysis.png' and 'volatility_surface_complete.png') saved in repo. 
3. three_arb_check: Tests for four different kinds of arbitrage: 
    - vertical spread: Calls with higher strikes should be less expensive. 
    - butterfly: Should cost money to buy. 
    - put call parity: Self explanatory. 
    - time spread: Longer dated options should cost more. 
    If an arbitrage is found, plots a heatmap to determine if arbitrage clusters around certain strikes/DTES. 
4. four_market_maker: Uses computed IV surfaces and computes Greeks to determine how to price an order of the user's choice. 
    Bid-ask spreads are widened for higher risk (determined by set Greek limits). Plots how prices of options 
    in nearby strikes/DTEs relate to the given order. An example is provided for a near-dated short ATM call. 