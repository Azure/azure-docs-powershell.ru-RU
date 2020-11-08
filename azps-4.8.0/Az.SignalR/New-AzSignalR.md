---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94087994"
---
# <span data-ttu-id="d2ef5-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d2ef5-101">New-AzSignalR</span></span>

## <span data-ttu-id="d2ef5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ef5-103">Создание службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-103">Create a SignalR service.</span></span>

## <span data-ttu-id="d2ef5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2ef5-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ef5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ef5-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ef5-106">Создание службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-106">Create a SignalR service.</span></span>
<span data-ttu-id="d2ef5-107">Если не указано, для параметров будут использоваться следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d2ef5-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="d2ef5-108">`ResourceGroupName`: Стандартная группа ресурсов, установленная по умолчанию `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="d2ef5-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="d2ef5-109">`Location`: расположение группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d2ef5-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="d2ef5-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="d2ef5-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="d2ef5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2ef5-111">EXAMPLES</span></span>

### <span data-ttu-id="d2ef5-112">Создание службы сигналов</span><span class="sxs-lookup"><span data-stu-id="d2ef5-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="d2ef5-113">Указание ServiceMode и AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="d2ef5-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="d2ef5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2ef5-114">PARAMETERS</span></span>

### <span data-ttu-id="d2ef5-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="d2ef5-115">-AllowedOrigin</span></span>
<span data-ttu-id="d2ef5-116">Разрешенные источники для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="d2ef5-117">Чтобы разрешить все, используйте "\*" и удалите все остальные источники из списка.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="d2ef5-118">Косые черты не разрешены как часть домена или после TLD</span><span class="sxs-lookup"><span data-stu-id="d2ef5-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="d2ef5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2ef5-119">-AsJob</span></span>
<span data-ttu-id="d2ef5-120">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d2ef5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ef5-121">-DefaultProfile</span></span>
<span data-ttu-id="d2ef5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ef5-123">-Location</span><span class="sxs-lookup"><span data-stu-id="d2ef5-123">-Location</span></span>
<span data-ttu-id="d2ef5-124">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-124">The SignalR service location.</span></span> <span data-ttu-id="d2ef5-125">Если не указано, будет использоваться расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="d2ef5-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2ef5-126">-Name</span></span>
<span data-ttu-id="d2ef5-127">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ef5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ef5-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2ef5-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-129">The resource group name.</span></span> <span data-ttu-id="d2ef5-130">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="d2ef5-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="d2ef5-131">-ServiceMode</span></span>
<span data-ttu-id="d2ef5-132">Режим обслуживания для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="d2ef5-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="d2ef5-133">-Sku</span></span>
<span data-ttu-id="d2ef5-134">SKU службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ef5-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="d2ef5-135">-Tag</span></span>
<span data-ttu-id="d2ef5-136">Теги для службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="d2ef5-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="d2ef5-137">-UnitCount</span></span>
<span data-ttu-id="d2ef5-138">Количество единиц услуги SignalR от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="d2ef5-139">По умолчанию используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ef5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ef5-140">-Confirm</span></span>
<span data-ttu-id="d2ef5-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ef5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ef5-142">-WhatIf</span></span>
<span data-ttu-id="d2ef5-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ef5-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ef5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ef5-145">CommonParameters</span></span>
<span data-ttu-id="d2ef5-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2ef5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ef5-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2ef5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ef5-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2ef5-148">INPUTS</span></span>

### <span data-ttu-id="d2ef5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ef5-149">System.String</span></span>

## <span data-ttu-id="d2ef5-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ef5-150">OUTPUTS</span></span>

### <span data-ttu-id="d2ef5-151">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d2ef5-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d2ef5-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2ef5-152">NOTES</span></span>

## <span data-ttu-id="d2ef5-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2ef5-153">RELATED LINKS</span></span>