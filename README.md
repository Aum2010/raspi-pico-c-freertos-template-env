# raspi-pico-c-freertos-template-env

Thank You Repo : https://github.com/lukstep/raspberry-pi-pico-docker-sdk 

Hardware : https://inex.co.th/home/product/ax-pico/ [ From Maker Faire ]

## Build Project

<img title="a title" alt="Alt text" src="/img/Build-FreeRTOS-demo.png">

## Configuration "settings.json" to Select Project

<img title="a title" alt="Alt text" src="/img/Build-Select-Project.png">

## Print on Terminal

<img title="a title" alt="Alt text" src="/img/hello-FreeRTOS.png">

## FreeRTOS Blink LED on GPIO15

<video width="320" height="240" controls>
  <source src="/img/document_6060147383767929824.mp4" type="video/mp4">
</video>

## Debugprobe

<img title="a title" alt="Alt text" src="/img/Picoprobe-Wiring.png">

https://github.com/raspberrypi/debugprobe
https://github.com/raspberrypi/debugprobe/releases

## xPack OpenOCD

https://github.com/xpack-dev-tools/openocd-xpack
https://github.com/xpack-dev-tools/openocd-xpack/releases

bash 

```

cd .\Desktop\xpack-openocd-0.12.0-2\
.\bin\openocd.exe -f interface\cmsis-dap.cfg -f target\rp2040.cfg -c 'bindto 0.0.0.0' -c 'adapter speed 5000' -c 'init'

```

<img title="a title" alt="Alt text" src="/img/OpenOCD.png">

## Update "launch.json"

```
    "inputs": [
        {
            "id": "ELF_PATH",
            "type": "command",
            "command": "shellCommand.execute",
            "args": {
                "command": "echo ./build/freertos_demo.elf", <------ To /*.elf
                "useFirstResult": "true"
            }
        }
    ],
```