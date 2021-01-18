---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518402"
---
# <span data-ttu-id="76b21-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="76b21-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="76b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b21-102">SYNOPSIS</span></span>
<span data-ttu-id="76b21-103">Вызов метода модуля Edge.</span><span class="sxs-lookup"><span data-stu-id="76b21-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="76b21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76b21-104">SYNTAX</span></span>

### <span data-ttu-id="76b21-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76b21-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76b21-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="76b21-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b21-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="76b21-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76b21-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76b21-108">DESCRIPTION</span></span>
<span data-ttu-id="76b21-109">Вызов метода модуля Edge.</span><span class="sxs-lookup"><span data-stu-id="76b21-109">Invoke an Edge module method.</span></span> <span data-ttu-id="76b21-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="76b21-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="76b21-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76b21-111">EXAMPLES</span></span>

### <span data-ttu-id="76b21-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76b21-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="76b21-113">Вызов метода модуля Edge.</span><span class="sxs-lookup"><span data-stu-id="76b21-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="76b21-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76b21-114">PARAMETERS</span></span>

### <span data-ttu-id="76b21-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="76b21-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="76b21-116">Количество секунд, необходимое для успешного подключения.</span><span class="sxs-lookup"><span data-stu-id="76b21-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="76b21-117">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="76b21-117">Default is 10.</span></span>

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

### <span data-ttu-id="76b21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b21-118">-DefaultProfile</span></span>
<span data-ttu-id="76b21-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76b21-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76b21-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="76b21-120">-DeviceId</span></span>
<span data-ttu-id="76b21-121">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="76b21-121">Target Device Id.</span></span>

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

### <span data-ttu-id="76b21-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76b21-122">-InputObject</span></span>
<span data-ttu-id="76b21-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="76b21-123">IotHub object</span></span>

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

### <span data-ttu-id="76b21-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="76b21-124">-IotHubName</span></span>
<span data-ttu-id="76b21-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="76b21-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="76b21-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="76b21-126">-ModuleId</span></span>
<span data-ttu-id="76b21-127">Модуль целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="76b21-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b21-128">-Name</span><span class="sxs-lookup"><span data-stu-id="76b21-128">-Name</span></span>
<span data-ttu-id="76b21-129">Имя метода, вызываемого в этом модуле устройства.</span><span class="sxs-lookup"><span data-stu-id="76b21-129">The name of the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="76b21-130">-Payload</span><span class="sxs-lookup"><span data-stu-id="76b21-130">-Payload</span></span>
<span data-ttu-id="76b21-131">Гружа для метода, вызываемого в этом модуле устройства.</span><span class="sxs-lookup"><span data-stu-id="76b21-131">The payload for the method to invoke on this device module.</span></span>

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

### <span data-ttu-id="76b21-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b21-132">-ResourceGroupName</span></span>
<span data-ttu-id="76b21-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="76b21-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="76b21-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76b21-134">-ResourceId</span></span>
<span data-ttu-id="76b21-135">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="76b21-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="76b21-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="76b21-136">-ResponseTimeOut</span></span>
<span data-ttu-id="76b21-137">Количество секунд, в течение первых нескольких секунд после получения результата непосредственного метода.</span><span class="sxs-lookup"><span data-stu-id="76b21-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="76b21-138">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="76b21-138">Default is 10.</span></span>

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

### <span data-ttu-id="76b21-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76b21-139">-Confirm</span></span>
<span data-ttu-id="76b21-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="76b21-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b21-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b21-141">-WhatIf</span></span>
<span data-ttu-id="76b21-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76b21-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b21-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76b21-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b21-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b21-144">CommonParameters</span></span>
<span data-ttu-id="76b21-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b21-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b21-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b21-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b21-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76b21-147">INPUTS</span></span>

### <span data-ttu-id="76b21-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="76b21-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="76b21-149">System.String</span><span class="sxs-lookup"><span data-stu-id="76b21-149">System.String</span></span>

## <span data-ttu-id="76b21-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76b21-150">OUTPUTS</span></span>

### <span data-ttu-id="76b21-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span><span class="sxs-lookup"><span data-stu-id="76b21-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="76b21-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76b21-152">NOTES</span></span>

## <span data-ttu-id="76b21-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76b21-153">RELATED LINKS</span></span>
