1. one_iv_computation: Loads SPY options data from Yahoo, takes a subset, loads into a dataframe. 
2. two_vol_surfaces: Uses the pricing data to compute implied volatility; plots surfaces and vol smiles. 
    figs (saved in repo) 
    - 'term_structure_analysis.png'
    - 'volatility_surface_complete.png'
3. three_arb_check: Tests for four different kinds of arbitrage: 
    - vertical spread: Calls with higher strikes should be less expensive. 
    - butterfly: Should cost money to buy. 
    - put call parity: Self explanatory. 
    - time spread: Longer dated options should cost more. 
4. four_market_maker: Uses computed IV surfaces and computes Greeks to determine how to price an order of the user's choice. 
    Bid-ask spreads are widened for higher risk (determined by set Greek limits). Plots how prices of options 
    in nearby strikes/DTEs relate to the given order. An example is provided for a near-dated short ATM call. 
5. trade_attractors: Implements a Markov chain choosing random orders and deciding whether or not to trade based on 
    a computed risk index. Then plots stationary distribution of Markov chain to investigate "attractors" in the state
    space of trades (ITM, OTM, or clustered around a particular time to expiration). 
    figs (saved in repo)
    - 'trading-attractor.png'
    - 'dist-over-expiry.png' 
    - 'dist-over-moneyness.png' 
    - 'attractor (by type).png' 
    