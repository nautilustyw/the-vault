#TheForge

This is an informal technical specification for Actions. It is an evolving document charting the long term vision. It is meant to be discussed, worked on, tested, improved, and implemented. 

The key is to begin small and build by taking experimental steps.

-   Action Name 
-   Action ID
-   Parent ID
-   Must support arbitrary combinations of data links: images, videos, GIFs, documents, …
	- Multiple of the same media should be supported. eg. An Action can be made up of 5 photos, 2 videos, 1 PDF document.
	- A Front Media to showcase the set. eg. Which image/GIF to show as the front cover?
- Actions must be extensible.
	- Extensibility provides flexibility. Actions can represent any activity this way.
	- LFF or 3rd parties can add their own metadata extend to specialize Actions.
	- Examples:
		-  colony membership Action: will turn Action into colony membership badge
		-  A colony creation Action will support colony info, reward-sharing agreement, parameters, etc.
-   Action Groups: Actions that are made up of multiple previously generated Actions 
	- Action groups allow Actions representing smaller activities to be represented within a greater whole.
-   Activity
	-   What does this action represent?
	-   eg. software development, running meetings, writing documentation, etc. 
	-   How do we allow for flexibility here without losing searchability, sortability etc.?
-   Action Type: [Predefined, trigger, custom]
	-   Predefined: Manual Action
	-   Trigger: triggered when a condition arrives
	-   Custom: API call etc.
-   Rarity
-   Colony Metadata 
	-   What colony has produced this Action?
	-   Any extra info about the colony.
-   Reward-Sharing Agreement (RSA)
	- Colony Reward Sharing Agreement Version: 0.1
	- This might be a reference to the agreement NFT
-   flC: littlefish coefficient 
	-   What percentage will each littlefish get from Action sales? 
	-   Set by the colony RSA
	-   Eg. 
		-   Action producer, colony members, colony wallet, LFF, Additional 3rd  
		-   70-10-10-10-0
	-   Range: 1 < x < 0
	-   Different coefficients for different littlefish: Producer, Buyer, etc.
	-   Support custom algorithms -> 1 to 0 varying
		-   Equilibrium - Selected by free market, trial and error
		-   Fibo 1/1 1/1 ½ ⅓ -> 10 10 5 3 2 1 <- Reward percentage per additional sale
-   Decay Rate:
	-   littlefish decay coefficient
		-   Set for each party in RSA
	-   Reward sharing rate decays at a rate set by the decay coefficient for each involved party.
		-   Decays are based on the last time each party has interacted with the colony. 
		-   Each interaction (buying or producing Action) will reset the decay coefficient to base. 
		-   Decay may be by time elapsed, or number of Actions since.``

