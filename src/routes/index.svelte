<script>
    let selection = {
        title: '',
        url: 'https://cloudcarpenter.com',
        icon: '',
        platform: 'win32',
        arch: 'x64'
    }
</script>

<header class="bg-blue-300 p-3 fixed top-0 left-0 w-full">
    <h1 class="text-4xl text-white">PWA Generator</h1>
</header>
<article class="bg-blue-300 py-20 h-screen">
    <div class="container mx-auto flex items-center gap-20">
        <div>
            <h2>Create Something Extraordinary</h2>
            <p>Enter a bit of information to generate your application.</p>
            <input bind:value={selection.title} type="text" placeholder="Application Title" class="block w-full p-3 rounded mb-3 text-sm">
            <input bind:value={selection.url} type="text" placeholder="URL" class="block w-full p-3 rounded mb-3 text-sm">
            <input bind:value={selection.icon} type="text" placeholder="Icon Path (.icns)" class="block w-full p-3 rounded mb-3 text-sm">
            <select bind:value={selection.platform} class="block w-full p-3 rounded mb-3 text-sm">
                <option value="win32">Windows</option>
                <option value="darwin">MacOS</option>
                <option value="linux">Linux</option>
            </select>
            <select bind:value={selection.arch} class="block w-full p-3 rounded text-sm mb-3">
                <option value="ia32">x86 (32 Bit)</option>
                <option value="x64">x64 (64 Bit)</option>
                <option value="armv7l">ARM v7 (32 Bit)</option>
                <option value="arm64">ARM (64 Bit)</option>
            </select>
            <button class="w-full bg-white/20 p-3 rounded border border-white text-sm ">
                Submit
            </button>
        </div>
        <div class="relative pointer-events-none">
            <img class="w-[800px]" src="/laptop.png" alt="Site Preview"/>
            <iframe class="absolute top-[10%] left-[15.5%] w-[70%] h-[73%]" src={selection.url} id="frame" scrolling="no" allowtransparency={false} title="Site Preview"></iframe>
        </div>
    </div>
</article>
<footer class="fixed bottom-0 left-0 w-full bg-gray-900 text-white p-3">
    A free application by <a class="text-blue-300" href="https://justinwhite.info" target="_blank">Justin White</a>
</footer>

<style>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>