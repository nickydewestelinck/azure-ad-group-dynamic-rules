# Azure AD GRoups - Dynamic Device rules
## All Windows Autopilot Devices
(device.devicePhysicalIDs -any (_ -contains "[ZTDID]"))

## All iPhone devices
(device.deviceOSType -eq "iPhone") 

## All iPad devices
(device.deviceOSType -eq "iPad")

## All Android Enterprise devices based on the enrollment profile
(device.enrollmentProfileName -eq "ENTER_AE_PROFILE_NAME_HERE")
