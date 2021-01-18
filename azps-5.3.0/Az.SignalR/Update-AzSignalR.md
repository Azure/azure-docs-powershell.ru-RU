---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505935"
---
# <span data-ttu-id="c604f-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="c604f-101">Update-AzSignalR</span></span>

## <span data-ttu-id="c604f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c604f-102">SYNOPSIS</span></span>
<span data-ttu-id="c604f-103">Обновив службу SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-103">Update a SignalR service.</span></span>

## <span data-ttu-id="c604f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c604f-104">SYNTAX</span></span>

### <span data-ttu-id="c604f-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c604f-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c604f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c604f-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c604f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c604f-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c604f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c604f-108">DESCRIPTION</span></span>
<span data-ttu-id="c604f-109">Обновив службу SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-109">Update a SignalR service.</span></span>
<span data-ttu-id="c604f-110">Следующие значения будут использоваться для параметров, если не указаны:</span><span class="sxs-lookup"><span data-stu-id="c604f-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="c604f-111">`ResourceGroupName`: группа ресурсов по умолчанию, установленная с помощью `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="c604f-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="c604f-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="c604f-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="c604f-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c604f-113">EXAMPLES</span></span>

### <span data-ttu-id="c604f-114">Обновление определенной службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="c604f-115">Укажите ServiceMode и AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="c604f-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="c604f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c604f-116">PARAMETERS</span></span>

### <span data-ttu-id="c604f-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="c604f-117">-AllowedOrigin</span></span>
<span data-ttu-id="c604f-118">Разрешенные источникы для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="c604f-119">Чтобы разрешить все, используйте "\*" и удалите из списка все остальные происхождение.</span><span class="sxs-lookup"><span data-stu-id="c604f-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="c604f-120">Косые черты не разрешены как часть домена или после TLD</span><span class="sxs-lookup"><span data-stu-id="c604f-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c604f-121">-AsJob</span></span>
<span data-ttu-id="c604f-122">Запустите проектлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="c604f-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="c604f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c604f-123">-DefaultProfile</span></span>
<span data-ttu-id="c604f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c604f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c604f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c604f-125">-InputObject</span></span>
<span data-ttu-id="c604f-126">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c604f-127">-Name</span></span>
<span data-ttu-id="c604f-128">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c604f-129">-ResourceGroupName</span></span>
<span data-ttu-id="c604f-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c604f-130">The resource group name.</span></span>
<span data-ttu-id="c604f-131">Значение по умолчанию будет использоваться, если не указано.</span><span class="sxs-lookup"><span data-stu-id="c604f-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c604f-132">-ResourceId</span></span>
<span data-ttu-id="c604f-133">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="c604f-134">-ServiceMode</span></span>
<span data-ttu-id="c604f-135">Режим обслуживания для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="c604f-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="c604f-136">-Sku</span></span>
<span data-ttu-id="c604f-137">SKU службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-137">The SignalR service SKU.</span></span>
<span data-ttu-id="c604f-138">Значение по умолчанию — "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="c604f-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="c604f-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="c604f-139">-Tag</span></span>
<span data-ttu-id="c604f-140">Теги для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="c604f-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="c604f-141">-UnitCount</span></span>
<span data-ttu-id="c604f-142">Единица сигнального устройства, значение только от {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="c604f-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="c604f-143">Значение по умолчанию 1.</span><span class="sxs-lookup"><span data-stu-id="c604f-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c604f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c604f-144">-Confirm</span></span>
<span data-ttu-id="c604f-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c604f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c604f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c604f-146">-WhatIf</span></span>
<span data-ttu-id="c604f-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c604f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c604f-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c604f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c604f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c604f-149">CommonParameters</span></span>
<span data-ttu-id="c604f-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c604f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c604f-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c604f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c604f-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c604f-152">INPUTS</span></span>

### <span data-ttu-id="c604f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c604f-153">System.String</span></span>

### <span data-ttu-id="c604f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c604f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c604f-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c604f-155">OUTPUTS</span></span>

### <span data-ttu-id="c604f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="c604f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="c604f-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c604f-157">NOTES</span></span>

## <span data-ttu-id="c604f-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c604f-158">RELATED LINKS</span></span>
