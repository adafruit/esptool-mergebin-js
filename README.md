# esptool-mergebin-js

A port of ESPTool's merge-bin option for use in JavaScript.

## Example Usage

```javascript
import { MergeBin } from 'https://cdn.jsdelivr.net/gh/adafruit/esptool-mergebin-js/mergebin.js?module';

let mergebin = new MergeBin();

// Optionally set some parameters (these are just examples)
mergebin.setFlashSize("8MB")
mergebin.setFlashFreq("40m")
mergebin.setFlashFreq("40m")
mergebin.setFlashMode("dio")

async doMerge() {}
    mergebin.addFile("bootloader.bin", 0x0000);
    mergebin.addFile("myfile.bin", 0x1000);

    let combined = await mergebin.generate("esp32");
    /*
    	  Do something with combined
    */
}
```

