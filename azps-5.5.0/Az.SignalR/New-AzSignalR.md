---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223097"
---
# <span data-ttu-id="93088-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="93088-101">New-AzSignalR</span></span>

## <span data-ttu-id="93088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93088-102">SYNOPSIS</span></span>
<span data-ttu-id="93088-103">Создайте службу SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-103">Create a SignalR service.</span></span>

## <span data-ttu-id="93088-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93088-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93088-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93088-105">DESCRIPTION</span></span>
<span data-ttu-id="93088-106">Создайте службу SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-106">Create a SignalR service.</span></span>
<span data-ttu-id="93088-107">Следующие значения будут использоваться для параметров, если не указаны:</span><span class="sxs-lookup"><span data-stu-id="93088-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="93088-108">`ResourceGroupName`: группа ресурсов по умолчанию, установленная с помощью `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="93088-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="93088-109">`Location`: расположение группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="93088-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="93088-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="93088-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="93088-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93088-111">EXAMPLES</span></span>

### <span data-ttu-id="93088-112">Создание службы SignalR</span><span class="sxs-lookup"><span data-stu-id="93088-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="93088-113">Укажите ServiceMode и AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="93088-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="93088-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93088-114">PARAMETERS</span></span>

### <span data-ttu-id="93088-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="93088-115">-AllowedOrigin</span></span>
<span data-ttu-id="93088-116">Разрешенные источникы для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="93088-117">Чтобы разрешить все, используйте "\*" и удалите из списка все остальные.</span><span class="sxs-lookup"><span data-stu-id="93088-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="93088-118">Косые черты не разрешены как часть домена или после TLD</span><span class="sxs-lookup"><span data-stu-id="93088-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="93088-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93088-119">-AsJob</span></span>
<span data-ttu-id="93088-120">Запустите его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="93088-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="93088-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93088-121">-DefaultProfile</span></span>
<span data-ttu-id="93088-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93088-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93088-123">-Location</span><span class="sxs-lookup"><span data-stu-id="93088-123">-Location</span></span>
<span data-ttu-id="93088-124">Расположение службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-124">The SignalR service location.</span></span> <span data-ttu-id="93088-125">Расположение группы ресурсов будет использоваться, если не указано.</span><span class="sxs-lookup"><span data-stu-id="93088-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="93088-126">-Name</span><span class="sxs-lookup"><span data-stu-id="93088-126">-Name</span></span>
<span data-ttu-id="93088-127">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="93088-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93088-128">-ResourceGroupName</span></span>
<span data-ttu-id="93088-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93088-129">The resource group name.</span></span> <span data-ttu-id="93088-130">Значение по умолчанию будет использоваться, если не указано.</span><span class="sxs-lookup"><span data-stu-id="93088-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="93088-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="93088-131">-ServiceMode</span></span>
<span data-ttu-id="93088-132">Режим обслуживания для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="93088-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="93088-133">-Sku</span></span>
<span data-ttu-id="93088-134">SKU службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="93088-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="93088-135">-Tag</span></span>
<span data-ttu-id="93088-136">Теги для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="93088-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="93088-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="93088-137">-UnitCount</span></span>
<span data-ttu-id="93088-138">Единица сигнального устройства от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="93088-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="93088-139">Значение по умолчанию 1.</span><span class="sxs-lookup"><span data-stu-id="93088-139">Default to 1.</span></span>

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

### <span data-ttu-id="93088-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93088-140">-Confirm</span></span>
<span data-ttu-id="93088-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93088-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93088-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93088-142">-WhatIf</span></span>
<span data-ttu-id="93088-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93088-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93088-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="93088-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93088-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93088-145">CommonParameters</span></span>
<span data-ttu-id="93088-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93088-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93088-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93088-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93088-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93088-148">INPUTS</span></span>

### <span data-ttu-id="93088-149">System.String</span><span class="sxs-lookup"><span data-stu-id="93088-149">System.String</span></span>

## <span data-ttu-id="93088-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93088-150">OUTPUTS</span></span>

### <span data-ttu-id="93088-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="93088-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="93088-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93088-152">NOTES</span></span>

## <span data-ttu-id="93088-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93088-153">RELATED LINKS</span></span>
