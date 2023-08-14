<script>
    import { LightSwitch } from '@skeletonlabs/skeleton';
	import { drawerStore } from '@skeletonlabs/skeleton';

    function drawerClose() {
		drawerStore.close();
	}
</script>

<nav class="nav-list flex justify-end text-right m-1 my-4 p-4">
    <ul>
		<li>
            <a
            class="btn hover:scale-110"
            href="/blog"
            on:click={drawerClose}
            >
            Blog
            </a>
        </li>
		<li>
            <a
            class="btn hover:scale-110"
            href="/contact"
            on:click={drawerClose}
            >
            Contact
            </a>
        </li>
        <li class="flex justify-end mx-4">
            <LightSwitch />
        </li>
    </ul>
</nav>