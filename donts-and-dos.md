# Dos and don'ts:

<table>
	<thead>
		<tr>
			<th align="left">Don'ts</th>
			<th align="left">Dos</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>pull to keep code sync</td>
			<td>rebase to keep code sync</td>
		</tr>
		<tr>
			<td>rebase on master (or dev)</td>
			<td>rebase on the branch you are currently working (the branch which is gonna get the latest changes</td>
		</tr>
		<tr>
			<td>merge without --no-ff</td>
			<td>merge with --no-ff</td>
		</tr>
		<tr>
			<td>use local copies for security</td>
			<td>push to a remote branch (you can create a new one)</td>
		</tr>
		<tr>
			<td>use graphic clients</td>
			<td>make your self confortable with the console</td>
		</tr>
		<tr>
			<td>do meaningless commits</td>
			<td>do commits that makes sense</td>
		</tr>
		<tr>
			<td>do tmp (or wip, test, etc) commits for "save" temporary changes</td>
			<td>use stash</td>
		</tr>
		<tr>
			<td>work on dev. or master</td>
			<td>create your own feature branch and keep it sync with rebase</td>
		</tr>
		<tr>
			<td>merge/push without reviewing your own code</td>
			<td>review your own code before and make sure your commit makes sense</td>
		</tr>
		<tr>
			<td>merge/push branches full of small and meaningless commits</td>
			<td>rebase before, squash and rewrite your commits with a proper commit message</td>
		</tr>	
	</tbody>
</table>