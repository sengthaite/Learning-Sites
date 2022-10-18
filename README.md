Flux and Redux
==============
+ Flux architecture by: Bill Fisher and Jing Chen at Facebook F8 conference in April 2014.
+ Unidirectional data flow
+ Actors:
	1. Action: a structure describing any change in the system like mouse clicks, timeout events, Ajax requests, etc.
	2. Dispatcher: a single point in the system where anyone can submit an action for handling
	3. Store: maintain the application state and react to commands from the dispatcher
+ Redux derived from Flux => there are a few distinctions between the two architectures.
	- Redux only has a single store that has no logic by itself
	- Actions are dispatched and handled directly be the store
	- Store passes the actions to state-changing functions called reducers
+ Redux terminology
	- Actions and Action Creator (function create action object)
	- Reducer: never modify the state; they always create a new copy with the needed modifications
	- Middleware: interceptor for actions before they reach the store
		* modify the actions
		* create more actions
		* suppress actions
	- Store: receive actions, pass them through all the registered middleware, then use reducers to calculate a new state and save it
+ General concepts
	- Pure function: with the same arguments => always get the same result
	- Impure function: use any variables not passed in as arguments or create side effects
	- Mutating object: Object.freeze() make object appears immutable but still not affect nested objects.
# Redux
