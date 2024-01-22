# Azure AD GRoups - Dynamic Device rules
## All Windows Autopilot Devices
(device.devicePhysicalIDs -any (_ -contains "[ZTDID]"))

## All iPhone devices
(device.deviceOSType -eq "iPhone") 

## All iPad devices
(device.deviceOSType -eq "iPad")

## All Android Enterprise devices based on the enrollment profile
(device.enrollmentProfileName -eq "ENTER_AE_PROFILE_NAME_HERE")

## All Intune Enabled Licensed Users (for E3/E5 licenses, based on de Intune A ServicePlan ID)
user.assignedPlans -any (assignedPlan.servicePlanId -eq "c1ec4a95-1f05-45b3-a911-aa3fa01094f5" -and assignedPlan.capabilityStatus -eq "Enabled")

## Dynamic Device GRoup based on Device Tag in Autopilot
(device.devicePhysicalIds -any (_ -eq "[OrderID]:GROUPTAG"))

## Dynamic User Group basec on M365 Apps for Enterprise Subscriptionµ
user.assignedPlans -any (assignedPlan.servicePlanId -eq "43de0ff5-c92c-492b-9116-175376d08c38" -and assignedPlan.capabilityStatus -eq "Enabled")
