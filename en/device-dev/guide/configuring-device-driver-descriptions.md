# Configuring Device Driver Descriptions<a name="EN-US_TOPIC_0000001158241515"></a>

You can configure the device driver description in the configuration file at  **./drivers/adapter/khdf/linux/hcs/device\_info/device\_info.hcs**.

The  **device\_info.hcs**  file contains all necessary information for registering drivers in the input driver model with the HDF. You do not need to make any modification for the information unless otherwise required in special scenarios. The private configuration data of each driver uses the  **deviceMatchAttr**  field to match the  **match\_attr**  field in the  **input\_config.hcs**  file.

The input-related content in the configuration file is as follows \(For details about these fields, see  [Driver Development](https://device.harmonyos.com/en/docs/develop/drive/oem_drive_hdfdev_load-0000001051276785)[Driver Development](../driver/driver-development.md)\):

```
input :: host {
            hostName = "input_host";
            priority = 100;
            device_input_manager :: device {              // Specify the device driver description of the input device manager.
                device0 :: deviceNode {
                    policy = 2;                           // Services are released to both the kernel space and the user space.
                    priority = 100;                       // The default priority for the input device manager is 100.
                    preload = 0;                          // Load the driver.
                    permission = 0660;                    // Specify the permission for the driver to create device nodes.
                    moduleName = "HDF_INPUT_MANAGER";     // Match the moduleName in the driver entry structure.
                    serviceName = "hdf_input_host";       // Specify the device node name to be generated by the HDF.
                    deviceMatchAttr = "";                 // Leave this field empty because private configuration data is not required by the input device manager currently.
                }
            }

            device_hdf_touch :: device {                  // Specify the device driver description of the input common driver.
                device0 :: deviceNode {
                    policy = 2;                           // Services are released to both the kernel space and the user space.
                    priority = 120;                       // The default priority for the input common driver is 120.
                    preload = 0;                          // Load the driver.
                    permission = 0660;                    // Specify the permission for the driver to create device nodes.
                    moduleName = "HDF_TOUCH";             // Match the moduleName in the driver entry structure.
                    serviceName = "hdf_input_event1";     // Specify the device node name to be generated by the HDF.
                    deviceMatchAttr = "touch_device1";    // Keep this value the same as the match_attr value in the private configuration data.
                }
            }

            device_touch_chip :: device {                 // Specify the device description of the input chip driver.
                device0 :: deviceNode {
                    policy = 0;                           // Services are not released to both the kernel space and the user space.
                    priority = 130;                       // The default priority for the input chip driver is 130.
                    preload = 0;                          // Load the driver.
                    permission = 0660;                    // Specify the permission for the driver to create device nodes.
                    moduleName = "HDF_TOUCH_GT911";       // Match the moduleName in the driver entry structure.
                    serviceName = "hdf_touch_gt911_service";// Specify the device node name to be generated by the HDF.
                    deviceMatchAttr = "zsj_gt911_5p5";    // Keep this value the same as the match_attr value in the private configuration data.
                }
            }
  }
```

Pay attention to the following fields in the configuration file:

**priority**: specifies the driver loading priority.

**preload**: specifies whether to load the driver.

**moduleName**: This value must be the same as the  **moduleName**  value in the driver entry structure.

**serviceName**: This value is used by the HDF to create a device node name.

**deviceMatchAttr**: This value must be the same as the  **match\_attr**  value in the private configuration data.

After the device descriptions are configured, the HDF matches the configuration with the code registered with the driver entry structure based on the  **moduleName**  field, ensuring that drivers can be loaded properly. If multiple drivers are configured, the  **priority**  field determines the loading sequence of each driver.

