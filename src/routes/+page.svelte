<script lang="ts">
	import type { RefresherCustomEvent, RefresherEventDetail } from '@ionic/core';

	function refresher(ev: RefresherCustomEvent) {
		console.log('Refreshed.', ev);
		setTimeout(() => {
			ev.target.complete();
		}, 2000);
	}
</script>

<ion-content class="ion-padding">
	<ion-refresher slot="fixed" on:ionRefresh={refresher}>
		<ion-refresher-content pulling-text="Pull to refresh" refreshing-text="Refreshing..." />
	</ion-refresher>

	<p>Pull this content down to trigger the refresh.</p>
</ion-content>
