# ORProject
<head>
	
	<meta charset="utf-8"><meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
	<meta name="description" content="">
	<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
	<meta name="apple-mobile-web-app-capable" content="yes">
	<meta name="apple-mobile-web-app-status-bar-style" content="black">
	<link rel="apple-touch-icon" href="images/icon.png">
	<link rel="stylesheet" type="text/css" href="main.css">
	<link rel="shortcut icon" href="/favicon.ico" type="image/x-icon">
	<link rel="icon" href="./favicon.ico" type="image/x-icon">
<title>Beer Game</title></head>
<body>
	<script src="main.min.js" async=""></script>
	<noscript>
		&lt;div class="browser-warning"&gt;
			&lt;h3&gt;Javascript disabled&lt;/h3&gt;
			You need to have Javascript enabled in order to view this simulation.&lt;br&gt;
			Please enable Javascript for your browser, and then reload this page.
		&lt;/div&gt;
	</noscript>


<div id="bptk-view-31" class="beergame perspective bptk-view"><!--       _         _
 _ __ ___ (_)___ ___(_) ___  _ __
| '_ ` _ \| / __/ __| |/ _ \| '_ \
| | | | | | \__ \__ \ | (_) | | | |
|_| |_| |_|_|___/___/_|\___/|_| |_|
-->
<div class="page mission flipout" bptk-data-role="game.currentRole.name" data-role="retailer">
	<h1>Beer Game</h1>
	<div bptk-tabview=""><div id="bptk-view-33" class="tabview bptk-view"><ul class="nav nav-tabs"><li class="active"><a><i class="fa fa-"></i> Rules</a></li><li><a><i class="fa fa-"></i> Objectives</a></li><li><a><i class="fa fa-"></i> Pitfalls</a></li><li><a><i class="fa fa-"></i> Interesting Facts</a></li></ul><div class="tab-content" bptk-yield="" style="height: 354px;"><br style="clear:both"><figure id="bptk-view-36" class="tab-pane fade bptk-view in active"><div class="scrollable">
				<p>
					You are a <strong>Retailer</strong>
					within a supply chain that delivers beer from a brewery via a
					distributor, a wholesaler and a retailer to the end consumer.

					Your challenge is to ensure that the consumers demand for beer
					is satisfied by managing your part of the supply chain
					that leads from your wholesaler
					to your customers, the end consumers.
				</p>
				<p>
					<span class="label label-primary">Rules</span>
					The rules of the game are simple – the game is played in 24 rounds, in every round of the game you
					perform the following four steps:
					</p><ul>
						<li>
							<b>Check deliveries.</b> Check how many units of beer are being
							delivered to you from your
							<!-- rivets: if game.roles.retailer --><span>wholesaler.</span>
							<!-- rivets: if game.roles.wholesaler -->
							<!-- rivets: if game.roles.distributor -->
							<!-- rivets: if game.roles.brewery -->
						</li>
						<li>
							<b>Check orders.</b> Check how many units of beer your
							<!-- rivets: if game.roles.retailer --><span>customers have</span>
							<!-- rivets: if game.roles.wholesaler -->
							<!-- rivets: if game.roles.distributor -->
							<!-- rivets: if game.roles.brewery -->
							ordered.
						</li>
						<li>
							<b>Deliver beer.</b> Deliver as much beer as you can to satisfy
							demand – in the game, this step will be performed for
							you automatically.
						</li>
						<li>
							<b>Make order decision.</b> Decide how many units of beer you need
							to order from your
							<!-- rivets: if game.roles.retailer --><span>wholesaler</span>
							<!-- rivets: if game.roles.wholesaler -->
							<!-- rivets: if game.roles.distributor -->
							<!-- rivets: if game.roles.brewery -->
							to keep your inventory stocked up and to
							ensure you have enough beer to meet future demands.
						</li>
					</ul>
				<p>

			</p>
			</div></figure><figure id="bptk-view-37" class="tab-pane fade bptk-view"><div class="scrollable">
				<p>
					<span class="label label-primary">Objective</span>
					</p><ul>
						<li>
							<b>Keep your inventory steady</b> You need to keep your inventory steady to ensure you 								   can deal with fluctuations in demand. Try to reach an inventory target of <b>250</b> 							   by the end of the game.
						</li>
						<li>
							<b>Keep your cost down</b> Both excess inventory and backorders increase your cost. 								   Keep your total cost below <b>$8.300</b>.
						</li>
						<li bptk-unless="game.isMultiplayer">
							<b>Keep overall cost down</b> Excessive order behaviour on your part will lead to 								   shocks in the supply chain, which increase overall supply chain cost. Ensure that 								   the total cost of the supply chain remains below <b>$29.300</b>.
						</li>
					</ul>
				<p></p>
			</div></figure><figure id="bptk-view-38" class="tab-pane fade bptk-view"><div class="scrollable">
				<p>There are some pitfalls that you need to be aware of during the game:</p>
				<ul>
					<li>
						<b>Delays.</b> Your demands for beer may not be fulfilled immediately – your supplier may also 								       be out of stock and will then have to pass is own order up the supply chain.
					</li>
					<li>
						<b>Shocks.</b> Excessive order behaviour may lead to shocks in the supply line, which 									increases the overall supply chain cost.
					</li>
					<li>
						<b>Inventory Costs.</b> If you order to many units of beer, your inventory costs will rise, 										because you will need more people to handle the beer and more storage 										space. The target level of beer units in your inventory is 400 units. 										Inventory cost you <i class="fa fa-usd"></i><b>{{game.simulator.lastresult.performanceControlling▸costPerItemInInventory}}</b>
					</li>
					<li>
						<b>Backorder Costs</b> If you order to few units of beer, you may not be able to supply your 										customer with enough beer. Backorders cost you <i class="fa fa-usd">
					</i><b>{{game.simulator.lastresult.performanceControlling▸costPerItemInBackorder}}</b> per unit.
					</li>

				</ul>
				<p>
					Initially the system is in a steady state - but the beer you are selling has suddently become popular 						among students, so the demand may suddenly change...
				</p>
			</div></figure><figure id="bptk-view-39" class="tab-pane fade bptk-view"><div class="scrollable">
				<p>Some interesting facts about the Beer Game:</p>
				<ul>
					<li>
						The Beer Game was developed in the 1960s at MIT to illustrate how difficult it is to manage 							dynamic systems.
					</li>
					<li>
						The game became well known in the 1990s after Peter Senge's description of it in his 	
						 world-wide best-selling book "The Fifth Discipline".
					</li>
					<li bptk-unless="game.isMultiplayer">
						The Beer Game is traditionally played with four players (brewery, distributor, wholesaler, 							retailer) either as a board game or using computers. In this single player edition, the order 							decisions of the brewery, the distributor and the wholesaler are made using an order policy 							implemented using System Dynamics.
					</li>
					<li bptk-unless="game.isMultiplayer">
						The game runs entirely in your browser, no data is transmitted to our web-server.
					</li>
				</ul>
			</div></figure></div></div></div>
	<div class="button" bptk-action="flip" style="touch-action: pan-y; -webkit-user-select: none; -webkit-user-drag: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0);">
		<span>
			
			<i class="fa fa-share"></i>
		</span>
	</div>
</div>


