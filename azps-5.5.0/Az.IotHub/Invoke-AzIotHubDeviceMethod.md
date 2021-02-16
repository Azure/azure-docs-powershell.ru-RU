---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226489"
---
# <span data-ttu-id="adf00-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="adf00-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="adf00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adf00-102">SYNOPSIS</span></span>
<span data-ttu-id="adf00-103">Вызов прямого метода на устройстве.</span><span class="sxs-lookup"><span data-stu-id="adf00-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="adf00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="adf00-104">SYNTAX</span></span>

### <span data-ttu-id="adf00-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adf00-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adf00-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="adf00-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adf00-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="adf00-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adf00-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adf00-108">DESCRIPTION</span></span>
<span data-ttu-id="adf00-109">Вызов прямого метода на устройстве.</span><span class="sxs-lookup"><span data-stu-id="adf00-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="adf00-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods сведения см. в этой информации.</span><span class="sxs-lookup"><span data-stu-id="adf00-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="adf00-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="adf00-111">EXAMPLES</span></span>

### <span data-ttu-id="adf00-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="adf00-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="adf00-113">Вызов метода устройства.</span><span class="sxs-lookup"><span data-stu-id="adf00-113">Invoke a device method.</span></span>

## <span data-ttu-id="adf00-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adf00-114">PARAMETERS</span></span>

### <span data-ttu-id="adf00-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="adf00-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="adf00-116">Количество секунд, необходимое для успешного подключения.</span><span class="sxs-lookup"><span data-stu-id="adf00-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="adf00-117">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="adf00-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf00-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf00-118">-DefaultProfile</span></span>
<span data-ttu-id="adf00-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adf00-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adf00-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="adf00-120">-DeviceId</span></span>
<span data-ttu-id="adf00-121">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="adf00-121">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf00-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adf00-122">-InputObject</span></span>
<span data-ttu-id="adf00-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="adf00-123">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adf00-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="adf00-124">-IotHubName</span></span>
<span data-ttu-id="adf00-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="adf00-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="adf00-126">-Name</span><span class="sxs-lookup"><span data-stu-id="adf00-126">-Name</span></span>
<span data-ttu-id="adf00-127">Имя метода, вызываемого на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="adf00-127">The name of the method to invoke on this device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf00-128">-Payload</span><span class="sxs-lookup"><span data-stu-id="adf00-128">-Payload</span></span>
<span data-ttu-id="adf00-129">Гружа при вызове метода на этом устройстве.</span><span class="sxs-lookup"><span data-stu-id="adf00-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="adf00-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adf00-130">-ResourceGroupName</span></span>
<span data-ttu-id="adf00-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="adf00-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="adf00-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adf00-132">-ResourceId</span></span>
<span data-ttu-id="adf00-133">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="adf00-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="adf00-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="adf00-134">-ResponseTimeOut</span></span>
<span data-ttu-id="adf00-135">Количество секунд, в течение нескольких секунд после получения результата непосредственного метода.</span><span class="sxs-lookup"><span data-stu-id="adf00-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="adf00-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="adf00-136">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf00-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adf00-137">-Confirm</span></span>
<span data-ttu-id="adf00-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="adf00-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adf00-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adf00-139">-WhatIf</span></span>
<span data-ttu-id="adf00-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adf00-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adf00-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="adf00-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adf00-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf00-142">CommonParameters</span></span>
<span data-ttu-id="adf00-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf00-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf00-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf00-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf00-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adf00-145">INPUTS</span></span>

### <span data-ttu-id="adf00-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="adf00-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="adf00-147">System.String</span><span class="sxs-lookup"><span data-stu-id="adf00-147">System.String</span></span>

## <span data-ttu-id="adf00-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="adf00-148">OUTPUTS</span></span>

### <span data-ttu-id="adf00-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="adf00-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="adf00-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="adf00-150">NOTES</span></span>

## <span data-ttu-id="adf00-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adf00-151">RELATED LINKS</span></span>
