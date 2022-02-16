<script>
    function toggle() {
        window.document.body.classList.toggle('dark-mode')
    }
    </script>
    <button on:click={toggle}>
        <slot/>
    </button>
    <style>
        button {
            color: white;
        }
        :global(body.dark-mode) button {
            color: white;
        }
    </style>