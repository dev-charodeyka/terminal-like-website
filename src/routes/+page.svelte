<script>
  import WhiteCat from '../lib/icons/WhiteCat.svelte';
  import WhiteCatAngry from '../lib/icons/WhiteCatAngry.svelte';
  import OctoCat from '../lib/icons/OctoCat.svelte';
  import ShrinkingSquare from '../lib/icons/ShrinkingSquare.svelte';
  import ExpansionSquare from '../lib/icons/ExpansionSquare.svelte';
  import Ghost from '../lib/icons/Ghost.svelte';
</script>

<!--------------------------------------------------------------- background ---------------------------------------------------------------->
<div class="w-screen h-screen bg-gradient-to-r from-gradientBg1 to-gradientBg2 flex flex-col items-center justify-center">
  <!------------------------------------------------------------ terminal container ------------------------------------------------------------>
  <div class="w-[700px] h-[500px] flex flex-col border-8 border-topbarBg rounded-lg bg-topbarBg">
    <!--------------------------------------------------------- Terminal's TopBar ------------------------------------------------------------->
    <div class="relative flex flex-col items-center">
      <!-- SVG Kitty on the top of terminal-->
      <div class="absolute -top-9">
        <WhiteCat className="w-10 h-auto" />
      </div>

      <div class="hidden absolute -top-14">
        <WhiteCatAngry className="w-14 h-auto" />
      </div>

      <!-- topbar of terminal -->
      <div class="w-full border-topbarBg flex justify-end items-center -mt-2 gap-3 pr-2 p-3">
        <!-- button to resize terminal -->

        <button 
          class="flex items-center justify-center rounded-full border-2 border-accentBlue bg-topbarBlue w-6 h-6 hover:bg-topbarViola">
          <ExpansionSquare className="w-3 h-3 text-terminalBg" />

          <ShrinkingSquare className="hidden w-6 h-6 text-terminalBg" />
        </button>

        <button class="flex items-center justify-center rounded-full box-border bg-topbarOrange border-2 border-accentOrange w-6 h-6 hover:bg-topbarGreen">
          <OctoCat className="w-4 h-4 text-terminalBg" />
        </button>

      </div>
    </div>

    <!-- terminal-area itself -->
    <div class="w-full flex-1 bg-terminalBg pt-2">
      <div class="flex gap-2 items-center justify-start">
        <Ghost className="w-6 h-6" />
        <span class="text-topbarViola font-bold text-xl">~</span>

        <!-- Terminal inputs area -->
        <input class="option-input" type="text" />
      </div>
    </div>
  </div>
</div>