---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 8c8240ed1df30dface1bdb2ce0b649bacf17d08a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729093"
---
# <span data-ttu-id="f0425-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="f0425-101">New-AzSignalR</span></span>

## <span data-ttu-id="f0425-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0425-102">SYNOPSIS</span></span>
<span data-ttu-id="f0425-103">Создание службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="f0425-103">Create a SignalR service.</span></span>

## <span data-ttu-id="f0425-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0425-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0425-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0425-105">DESCRIPTION</span></span>
<span data-ttu-id="f0425-106">Создание службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="f0425-106">Create a SignalR service.</span></span>
<span data-ttu-id="f0425-107">Если не указано, для параметров будут использоваться следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f0425-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="f0425-108">`ResourceGroupName`: Стандартная группа ресурсов, установленная по умолчанию `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="f0425-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="f0425-109">`Location`: расположение группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0425-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="f0425-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="f0425-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="f0425-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0425-111">EXAMPLES</span></span>

### <span data-ttu-id="f0425-112">Создание поsignalr</span><span class="sxs-lookup"><span data-stu-id="f0425-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="f0425-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0425-113">PARAMETERS</span></span>

### <span data-ttu-id="f0425-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0425-114">-AsJob</span></span>
<span data-ttu-id="f0425-115">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="f0425-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="f0425-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0425-116">-DefaultProfile</span></span>
<span data-ttu-id="f0425-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0425-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0425-118">-Location</span><span class="sxs-lookup"><span data-stu-id="f0425-118">-Location</span></span>
<span data-ttu-id="f0425-119">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="f0425-119">The SignalR service location.</span></span> <span data-ttu-id="f0425-120">Если не указано, будет использоваться расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0425-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="f0425-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0425-121">-Name</span></span>
<span data-ttu-id="f0425-122">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="f0425-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="f0425-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0425-123">-ResourceGroupName</span></span>
<span data-ttu-id="f0425-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0425-124">The resource group name.</span></span> <span data-ttu-id="f0425-125">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="f0425-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="f0425-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="f0425-126">-Sku</span></span>
<span data-ttu-id="f0425-127">SKU службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="f0425-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="f0425-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="f0425-128">-Tag</span></span>
<span data-ttu-id="f0425-129">Теги для службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="f0425-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="f0425-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="f0425-130">-UnitCount</span></span>
<span data-ttu-id="f0425-131">Количество единиц услуги SignalR от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="f0425-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="f0425-132">По умолчанию используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="f0425-132">Default to 1.</span></span>

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

### <span data-ttu-id="f0425-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0425-133">-Confirm</span></span>
<span data-ttu-id="f0425-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0425-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0425-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0425-135">-WhatIf</span></span>
<span data-ttu-id="f0425-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0425-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0425-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0425-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0425-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0425-138">CommonParameters</span></span>
<span data-ttu-id="f0425-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0425-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0425-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0425-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0425-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0425-141">INPUTS</span></span>

### <span data-ttu-id="f0425-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0425-142">None</span></span>

## <span data-ttu-id="f0425-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0425-143">OUTPUTS</span></span>

### <span data-ttu-id="f0425-144">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f0425-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="f0425-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0425-145">NOTES</span></span>

## <span data-ttu-id="f0425-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0425-146">RELATED LINKS</span></span>
