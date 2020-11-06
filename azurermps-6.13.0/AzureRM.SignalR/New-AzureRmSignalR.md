---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
ms.openlocfilehash: d5b7e5480ea3078dadf5280b4f683280dcd00ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565346"
---
# <span data-ttu-id="b8fcb-101">New-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="b8fcb-101">New-AzureRmSignalR</span></span>

## <span data-ttu-id="b8fcb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fcb-103">Создание службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-103">Create a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8fcb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8fcb-104">SYNTAX</span></span>

```
New-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8fcb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="b8fcb-106">Создание службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-106">Create a SignalR service.</span></span>
<span data-ttu-id="b8fcb-107">Если не указано, для параметров будут использоваться следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b8fcb-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="b8fcb-108">`ResourceGroupName`: Стандартная группа ресурсов, установленная по умолчанию `Set-AzureRmDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="b8fcb-108">`ResourceGroupName`: the default resource group set by `Set-AzureRmDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="b8fcb-109">`Location`: расположение группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8fcb-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="b8fcb-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="b8fcb-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="b8fcb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8fcb-111">EXAMPLES</span></span>

### <span data-ttu-id="b8fcb-112">Создание поsignalr</span><span class="sxs-lookup"><span data-stu-id="b8fcb-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzureRmSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="b8fcb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8fcb-113">PARAMETERS</span></span>

### <span data-ttu-id="b8fcb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8fcb-114">-AsJob</span></span>
<span data-ttu-id="b8fcb-115">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="b8fcb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8fcb-116">-DefaultProfile</span></span>
<span data-ttu-id="b8fcb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8fcb-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b8fcb-118">-Location</span></span>
<span data-ttu-id="b8fcb-119">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-119">The SignalR service location.</span></span> <span data-ttu-id="b8fcb-120">Если не указано, будет использоваться расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="b8fcb-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8fcb-121">-Name</span></span>
<span data-ttu-id="b8fcb-122">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="b8fcb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fcb-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8fcb-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-124">The resource group name.</span></span> <span data-ttu-id="b8fcb-125">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="b8fcb-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="b8fcb-126">-Sku</span></span>
<span data-ttu-id="b8fcb-127">SKU службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="b8fcb-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="b8fcb-128">-Tag</span></span>
<span data-ttu-id="b8fcb-129">Теги для службы сигналов.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="b8fcb-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="b8fcb-130">-UnitCount</span></span>
<span data-ttu-id="b8fcb-131">Количество единиц услуги SignalR от 1 до 10.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="b8fcb-132">По умолчанию используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-132">Default to 1.</span></span>

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

### <span data-ttu-id="b8fcb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8fcb-133">-Confirm</span></span>
<span data-ttu-id="b8fcb-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8fcb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8fcb-135">-WhatIf</span></span>
<span data-ttu-id="b8fcb-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8fcb-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8fcb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8fcb-138">CommonParameters</span></span>
<span data-ttu-id="b8fcb-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8fcb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8fcb-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8fcb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8fcb-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8fcb-141">INPUTS</span></span>

### <span data-ttu-id="b8fcb-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="b8fcb-142">None</span></span>

## <span data-ttu-id="b8fcb-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8fcb-143">OUTPUTS</span></span>

### <span data-ttu-id="b8fcb-144">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b8fcb-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="b8fcb-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8fcb-145">NOTES</span></span>

## <span data-ttu-id="b8fcb-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8fcb-146">RELATED LINKS</span></span>
