---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235854"
---
# <span data-ttu-id="e9889-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="e9889-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="e9889-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9889-102">SYNOPSIS</span></span>
<span data-ttu-id="e9889-103">Удалите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="e9889-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="e9889-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9889-104">SYNTAX</span></span>

### <span data-ttu-id="e9889-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9889-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9889-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9889-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9889-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9889-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9889-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9889-108">DESCRIPTION</span></span>
<span data-ttu-id="e9889-109">Удалите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="e9889-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="e9889-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9889-110">EXAMPLES</span></span>

### <span data-ttu-id="e9889-111">Удаление службы SignalR</span><span class="sxs-lookup"><span data-stu-id="e9889-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="e9889-112">Удаление всех сигнальных служб в канале</span><span class="sxs-lookup"><span data-stu-id="e9889-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="e9889-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9889-113">PARAMETERS</span></span>

### <span data-ttu-id="e9889-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9889-114">-AsJob</span></span>
<span data-ttu-id="e9889-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e9889-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9889-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9889-116">-DefaultProfile</span></span>
<span data-ttu-id="e9889-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9889-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9889-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9889-118">-InputObject</span></span>
<span data-ttu-id="e9889-119">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="e9889-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="e9889-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9889-120">-Name</span></span>
<span data-ttu-id="e9889-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="e9889-121">SignalR service name.</span></span>

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

### <span data-ttu-id="e9889-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9889-122">-PassThru</span></span>
<span data-ttu-id="e9889-123">Возвращает значение истина, если удаление было успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="e9889-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9889-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9889-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9889-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9889-125">Resource group name.</span></span>

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

### <span data-ttu-id="e9889-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9889-126">-ResourceId</span></span>
<span data-ttu-id="e9889-127">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="e9889-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="e9889-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9889-128">-Confirm</span></span>
<span data-ttu-id="e9889-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9889-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9889-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9889-130">-WhatIf</span></span>
<span data-ttu-id="e9889-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9889-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9889-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9889-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9889-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9889-133">CommonParameters</span></span>
<span data-ttu-id="e9889-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9889-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9889-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9889-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9889-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9889-136">INPUTS</span></span>

### <span data-ttu-id="e9889-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e9889-137">System.String</span></span>
### <span data-ttu-id="e9889-138">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="e9889-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="e9889-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9889-139">OUTPUTS</span></span>

### <span data-ttu-id="e9889-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9889-140">System.Boolean</span></span>
## <span data-ttu-id="e9889-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9889-141">NOTES</span></span>

## <span data-ttu-id="e9889-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9889-142">RELATED LINKS</span></span>
