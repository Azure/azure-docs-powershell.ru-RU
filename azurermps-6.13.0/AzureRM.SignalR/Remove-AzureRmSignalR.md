---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565342"
---
# <span data-ttu-id="5b1d4-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="5b1d4-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="5b1d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1d4-103">Удалите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b1d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b1d4-104">SYNTAX</span></span>

### <span data-ttu-id="5b1d4-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b1d4-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1d4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1d4-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b1d4-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b1d4-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b1d4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b1d4-108">DESCRIPTION</span></span>
<span data-ttu-id="5b1d4-109">Удалите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="5b1d4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b1d4-110">EXAMPLES</span></span>

### <span data-ttu-id="5b1d4-111">Удаление службы SignalR</span><span class="sxs-lookup"><span data-stu-id="5b1d4-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="5b1d4-112">Удаление всех сигнальных служб в канале</span><span class="sxs-lookup"><span data-stu-id="5b1d4-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="5b1d4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b1d4-113">PARAMETERS</span></span>

### <span data-ttu-id="5b1d4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b1d4-114">-AsJob</span></span>
<span data-ttu-id="5b1d4-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5b1d4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b1d4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1d4-116">-DefaultProfile</span></span>
<span data-ttu-id="5b1d4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1d4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b1d4-118">-InputObject</span></span>
<span data-ttu-id="5b1d4-119">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5b1d4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b1d4-120">-Name</span></span>
<span data-ttu-id="5b1d4-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-121">SignalR service name.</span></span>

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

### <span data-ttu-id="5b1d4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b1d4-122">-PassThru</span></span>
<span data-ttu-id="5b1d4-123">Возвращает значение истина, если удаление было успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="5b1d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="5b1d4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-125">Resource group name.</span></span>

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

### <span data-ttu-id="5b1d4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1d4-126">-ResourceId</span></span>
<span data-ttu-id="5b1d4-127">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5b1d4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b1d4-128">-Confirm</span></span>
<span data-ttu-id="5b1d4-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b1d4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b1d4-130">-WhatIf</span></span>
<span data-ttu-id="5b1d4-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b1d4-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b1d4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1d4-133">CommonParameters</span></span>
<span data-ttu-id="5b1d4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b1d4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1d4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b1d4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1d4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b1d4-136">INPUTS</span></span>

### <span data-ttu-id="5b1d4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5b1d4-137">System.String</span></span>
<span data-ttu-id="5b1d4-138">Параметры: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b1d4-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="5b1d4-139">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="5b1d4-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="5b1d4-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b1d4-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5b1d4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b1d4-141">OUTPUTS</span></span>

### <span data-ttu-id="5b1d4-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b1d4-142">System.Boolean</span></span>

## <span data-ttu-id="5b1d4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b1d4-143">NOTES</span></span>

## <span data-ttu-id="5b1d4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b1d4-144">RELATED LINKS</span></span>
