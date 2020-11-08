---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236614"
---
# <span data-ttu-id="1aa13-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="1aa13-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="1aa13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1aa13-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa13-103">Повторное создание клавиши доступа для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="1aa13-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="1aa13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1aa13-104">SYNTAX</span></span>

### <span data-ttu-id="1aa13-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1aa13-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa13-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa13-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aa13-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aa13-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa13-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aa13-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa13-109">Повторное создание клавиши доступа для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="1aa13-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="1aa13-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1aa13-110">EXAMPLES</span></span>

### <span data-ttu-id="1aa13-111">Повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="1aa13-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="1aa13-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1aa13-112">PARAMETERS</span></span>

### <span data-ttu-id="1aa13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa13-113">-DefaultProfile</span></span>
<span data-ttu-id="1aa13-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1aa13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aa13-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aa13-115">-InputObject</span></span>
<span data-ttu-id="1aa13-116">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="1aa13-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="1aa13-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1aa13-117">-KeyType</span></span>
<span data-ttu-id="1aa13-118">Тип ключа: Primary или Secondary.</span><span class="sxs-lookup"><span data-stu-id="1aa13-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa13-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1aa13-119">-Name</span></span>
<span data-ttu-id="1aa13-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="1aa13-120">SignalR service name.</span></span>

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

### <span data-ttu-id="1aa13-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1aa13-121">-PassThru</span></span>
<span data-ttu-id="1aa13-122">Возвращает значение "истина", если повторное создание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="1aa13-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="1aa13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa13-123">-ResourceGroupName</span></span>
<span data-ttu-id="1aa13-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1aa13-124">Resource group name.</span></span>

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

### <span data-ttu-id="1aa13-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aa13-125">-ResourceId</span></span>
<span data-ttu-id="1aa13-126">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="1aa13-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="1aa13-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aa13-127">-Confirm</span></span>
<span data-ttu-id="1aa13-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1aa13-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa13-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa13-129">-WhatIf</span></span>
<span data-ttu-id="1aa13-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1aa13-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa13-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1aa13-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa13-132">CommonParameters</span></span>
<span data-ttu-id="1aa13-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1aa13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa13-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aa13-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa13-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1aa13-135">INPUTS</span></span>

### <span data-ttu-id="1aa13-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1aa13-136">System.String</span></span>
### <span data-ttu-id="1aa13-137">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1aa13-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="1aa13-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aa13-138">OUTPUTS</span></span>

### <span data-ttu-id="1aa13-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1aa13-139">System.Boolean</span></span>
## <span data-ttu-id="1aa13-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="1aa13-140">NOTES</span></span>

## <span data-ttu-id="1aa13-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aa13-141">RELATED LINKS</span></span>
