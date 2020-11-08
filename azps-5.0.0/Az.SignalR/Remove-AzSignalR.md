---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247528"
---
# <span data-ttu-id="51854-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="51854-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="51854-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51854-102">SYNOPSIS</span></span>
<span data-ttu-id="51854-103">Удалите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="51854-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="51854-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51854-104">SYNTAX</span></span>

### <span data-ttu-id="51854-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51854-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51854-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51854-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51854-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51854-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51854-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51854-108">DESCRIPTION</span></span>
<span data-ttu-id="51854-109">Удалите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="51854-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="51854-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51854-110">EXAMPLES</span></span>

### <span data-ttu-id="51854-111">Удаление службы SignalR</span><span class="sxs-lookup"><span data-stu-id="51854-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="51854-112">Удаление всех сигнальных служб в канале</span><span class="sxs-lookup"><span data-stu-id="51854-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="51854-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51854-113">PARAMETERS</span></span>

### <span data-ttu-id="51854-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51854-114">-AsJob</span></span>
<span data-ttu-id="51854-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="51854-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51854-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51854-116">-DefaultProfile</span></span>
<span data-ttu-id="51854-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51854-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51854-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51854-118">-InputObject</span></span>
<span data-ttu-id="51854-119">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="51854-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="51854-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51854-120">-Name</span></span>
<span data-ttu-id="51854-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="51854-121">SignalR service name.</span></span>

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

### <span data-ttu-id="51854-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51854-122">-PassThru</span></span>
<span data-ttu-id="51854-123">Возвращает значение истина, если удаление было успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="51854-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="51854-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51854-124">-ResourceGroupName</span></span>
<span data-ttu-id="51854-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51854-125">Resource group name.</span></span>

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

### <span data-ttu-id="51854-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51854-126">-ResourceId</span></span>
<span data-ttu-id="51854-127">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="51854-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="51854-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51854-128">-Confirm</span></span>
<span data-ttu-id="51854-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51854-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51854-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51854-130">-WhatIf</span></span>
<span data-ttu-id="51854-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51854-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51854-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51854-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51854-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51854-133">CommonParameters</span></span>
<span data-ttu-id="51854-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51854-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51854-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51854-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51854-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51854-136">INPUTS</span></span>

### <span data-ttu-id="51854-137">System. String</span><span class="sxs-lookup"><span data-stu-id="51854-137">System.String</span></span>
### <span data-ttu-id="51854-138">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="51854-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="51854-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51854-139">OUTPUTS</span></span>

### <span data-ttu-id="51854-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51854-140">System.Boolean</span></span>
## <span data-ttu-id="51854-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="51854-141">NOTES</span></span>

## <span data-ttu-id="51854-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51854-142">RELATED LINKS</span></span>
