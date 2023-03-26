<script>
  export let color = "red",
    rounded = false,
    large = false,
    translucent = false,
    blurry = false;

  let background = translucent ? "bg-red-600/50" : "bg-red-600",
    border = "border-red-500",
    text = "text-neutral-50",
    size = "py-1 px-3",
    round = "rounded",
    shadow = "hover:shadow-red-500 hover:shadow-xl",
    blur = "";

  if (rounded) round = "rounded-full";

  if (large) size = "py-2 px-6";

  if (blurry) blur = "backdrop-blur-xl";

  switch (color) {
    case "red":
      background = translucent ? "bg-red-600/50" : "bg-red-600";
      border = "border-red-500";
      text = translucent ? "dark:text-neutral-50 text-neutral-900" : "text-neutral-50";
      shadow = translucent ? "hover:shadow-red-500/60 hover:shadow-xl" : "hover:shadow-red-500 hover:shadow-xl";
      break;

    case "amber":
      background = translucent ? "bg-amber-400/50" : "bg-amber-400";
      border = "border-amber-300";
      text = translucent ? "dark:text-neutral-50 text-neutral-900" : "text-neutral-900";
      shadow = translucent ? "hover:shadow-amber-300/60 hover:shadow-xl" : "hover:shadow-amber-300 hover:shadow-xl";
      break;

    case "black":
      background = translucent ? "bg-neutral-900/50" : "bg-neutral-900";
      border = "border-neutral-800";
      text = "text-neutral-50";
      shadow = translucent ? "hover:shadow-neutral-800/50 hover:shadow-xl" : "hover:shadow-neutral-800 hover:shadow-xl";
      break;

    case "white":
      background = translucent ? "bg-neutral-100/30" : "bg-neutral-100";
      border = "border-neutral-200";
      text = translucent ? "dark:text-neutral-50 text-neutral-900" : "text-neutral-900";
      shadow = translucent ? "hover:shadow-neutral-50/50 hover:shadow-xl" : "hover:shadow-neutral-50 hover:shadow-xl";
      break;
  }

  let classes = `${background} ${border} ${text} ${size} ${shadow} ${round} ${blur}`;
  classes += " border shadow duration-200";
</script>

<button class={classes}><slot /></button>