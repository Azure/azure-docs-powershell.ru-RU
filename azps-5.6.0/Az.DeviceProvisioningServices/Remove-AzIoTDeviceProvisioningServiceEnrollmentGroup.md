---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 9b27875e19837d7e3b69770234bdcd19648c3130
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985158"
---
# <span data-ttu-id="df8c0-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="df8c0-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="df8c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="df8c0-103">Удаление группы регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="df8c0-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="df8c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df8c0-104">SYNTAX</span></span>

### <span data-ttu-id="df8c0-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df8c0-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df8c0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df8c0-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df8c0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df8c0-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df8c0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df8c0-108">DESCRIPTION</span></span>
<span data-ttu-id="df8c0-109">Удалите группу регистрации в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="df8c0-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="df8c0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df8c0-110">EXAMPLES</span></span>

### <span data-ttu-id="df8c0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df8c0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="df8c0-112">Удаление указанной группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="df8c0-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="df8c0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df8c0-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="df8c0-114">Удалите все группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="df8c0-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="df8c0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df8c0-115">PARAMETERS</span></span>

### <span data-ttu-id="df8c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8c0-116">-DefaultProfile</span></span>
<span data-ttu-id="df8c0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df8c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="df8c0-118">-DpsName</span></span>
<span data-ttu-id="df8c0-119">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="df8c0-119">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="df8c0-120">-DpsObject</span></span>
<span data-ttu-id="df8c0-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="df8c0-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="df8c0-122">-Name</span></span>
<span data-ttu-id="df8c0-123">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="df8c0-123">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df8c0-124">-PassThru</span></span>
<span data-ttu-id="df8c0-125">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="df8c0-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="df8c0-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="df8c0-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df8c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="df8c0-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="df8c0-128">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df8c0-129">-ResourceId</span></span>
<span data-ttu-id="df8c0-130">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="df8c0-130">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df8c0-131">-Confirm</span></span>
<span data-ttu-id="df8c0-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="df8c0-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8c0-133">-WhatIf</span></span>
<span data-ttu-id="df8c0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df8c0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8c0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="df8c0-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8c0-136">CommonParameters</span></span>
<span data-ttu-id="df8c0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df8c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8c0-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df8c0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8c0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df8c0-139">INPUTS</span></span>

### <span data-ttu-id="df8c0-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="df8c0-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="df8c0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="df8c0-141">System.String</span></span>

## <span data-ttu-id="df8c0-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df8c0-142">OUTPUTS</span></span>

### <span data-ttu-id="df8c0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="df8c0-143">System.Boolean</span></span>

## <span data-ttu-id="df8c0-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df8c0-144">NOTES</span></span>

## <span data-ttu-id="df8c0-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df8c0-145">RELATED LINKS</span></span>
