---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: fd39f75cd40f36f61af34ef2233a2e91072bafba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905245"
---
# <span data-ttu-id="8478f-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="8478f-101">Update-AzSignalR</span></span>

## <span data-ttu-id="8478f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8478f-102">SYNOPSIS</span></span>
<span data-ttu-id="8478f-103">Обновите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="8478f-103">Update a SignalR service.</span></span>

## <span data-ttu-id="8478f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8478f-104">SYNTAX</span></span>

### <span data-ttu-id="8478f-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8478f-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8478f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8478f-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8478f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8478f-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8478f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8478f-108">DESCRIPTION</span></span>
<span data-ttu-id="8478f-109">Обновите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="8478f-109">Update a SignalR service.</span></span>
<span data-ttu-id="8478f-110">Если не указано, для параметров будут использоваться следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8478f-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="8478f-111">`ResourceGroupName`: Стандартная группа ресурсов, установленная по умолчанию `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="8478f-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="8478f-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="8478f-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="8478f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8478f-113">EXAMPLES</span></span>

### <span data-ttu-id="8478f-114">Обновите специальную службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="8478f-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="8478f-115">Указание ServiceMode и AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="8478f-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="8478f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8478f-116">PARAMETERS</span></span>

### <span data-ttu-id="8478f-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="8478f-117">-AllowedOrigin</span></span>
<span data-ttu-id="8478f-118">Разрешенные источники для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="8478f-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="8478f-119">Чтобы разрешить все, используйте "\*" и удалите все остальные источники из списка.</span><span class="sxs-lookup"><span data-stu-id="8478f-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="8478f-120">Косые черты не разрешены как часть домена или после TLD</span><span class="sxs-lookup"><span data-stu-id="8478f-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="8478f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8478f-121">-AsJob</span></span>
<span data-ttu-id="8478f-122">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="8478f-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="8478f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8478f-123">-DefaultProfile</span></span>
<span data-ttu-id="8478f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8478f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8478f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8478f-125">-InputObject</span></span>
<span data-ttu-id="8478f-126">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="8478f-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="8478f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8478f-127">-Name</span></span>
<span data-ttu-id="8478f-128">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="8478f-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="8478f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8478f-129">-ResourceGroupName</span></span>
<span data-ttu-id="8478f-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8478f-130">The resource group name.</span></span>
<span data-ttu-id="8478f-131">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="8478f-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="8478f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8478f-132">-ResourceId</span></span>
<span data-ttu-id="8478f-133">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="8478f-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8478f-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="8478f-134">-ServiceMode</span></span>
<span data-ttu-id="8478f-135">Режим обслуживания для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="8478f-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="8478f-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="8478f-136">-Sku</span></span>
<span data-ttu-id="8478f-137">SKU службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="8478f-137">The SignalR service SKU.</span></span>
<span data-ttu-id="8478f-138">По умолчанию используется значение "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="8478f-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="8478f-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="8478f-139">-Tag</span></span>
<span data-ttu-id="8478f-140">Теги для службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="8478f-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="8478f-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="8478f-141">-UnitCount</span></span>
<span data-ttu-id="8478f-142">Счетчик единиц услуги SignalR имеет значение только от {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="8478f-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="8478f-143">По умолчанию используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="8478f-143">Default to 1.</span></span>

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

### <span data-ttu-id="8478f-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8478f-144">-Confirm</span></span>
<span data-ttu-id="8478f-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8478f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8478f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8478f-146">-WhatIf</span></span>
<span data-ttu-id="8478f-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8478f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8478f-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8478f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8478f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8478f-149">CommonParameters</span></span>
<span data-ttu-id="8478f-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8478f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8478f-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8478f-151">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8478f-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8478f-152">INPUTS</span></span>

### <span data-ttu-id="8478f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8478f-153">System.String</span></span>

### <span data-ttu-id="8478f-154">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="8478f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="8478f-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8478f-155">OUTPUTS</span></span>

### <span data-ttu-id="8478f-156">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="8478f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="8478f-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="8478f-157">NOTES</span></span>

## <span data-ttu-id="8478f-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8478f-158">RELATED LINKS</span></span>
