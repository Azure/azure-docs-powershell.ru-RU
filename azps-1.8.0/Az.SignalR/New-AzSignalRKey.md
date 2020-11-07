---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 3feb052875cdf9afa7a32d4e7fc8066517b16dd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729090"
---
# <span data-ttu-id="3ea95-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="3ea95-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="3ea95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ea95-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea95-103">Повторное создание клавиши доступа для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="3ea95-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="3ea95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ea95-104">SYNTAX</span></span>

### <span data-ttu-id="3ea95-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ea95-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea95-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea95-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea95-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea95-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea95-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ea95-108">DESCRIPTION</span></span>
<span data-ttu-id="3ea95-109">Повторное создание клавиши доступа для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="3ea95-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="3ea95-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ea95-110">EXAMPLES</span></span>

### <span data-ttu-id="3ea95-111">Повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="3ea95-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="3ea95-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ea95-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea95-113">-DefaultProfile</span></span>
<span data-ttu-id="3ea95-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea95-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ea95-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ea95-115">-InputObject</span></span>
<span data-ttu-id="3ea95-116">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="3ea95-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="3ea95-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3ea95-117">-KeyType</span></span>
<span data-ttu-id="3ea95-118">Тип ключа: Primary или Secondary.</span><span class="sxs-lookup"><span data-stu-id="3ea95-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="3ea95-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ea95-119">-Name</span></span>
<span data-ttu-id="3ea95-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="3ea95-120">SignalR service name.</span></span>

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

### <span data-ttu-id="3ea95-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ea95-121">-PassThru</span></span>
<span data-ttu-id="3ea95-122">Возвращает значение "истина", если повторное создание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="3ea95-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="3ea95-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea95-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ea95-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ea95-124">Resource group name.</span></span>

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

### <span data-ttu-id="3ea95-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea95-125">-ResourceId</span></span>
<span data-ttu-id="3ea95-126">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="3ea95-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="3ea95-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ea95-127">-Confirm</span></span>
<span data-ttu-id="3ea95-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ea95-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea95-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea95-129">-WhatIf</span></span>
<span data-ttu-id="3ea95-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ea95-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea95-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ea95-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea95-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea95-132">CommonParameters</span></span>
<span data-ttu-id="3ea95-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ea95-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea95-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea95-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea95-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ea95-135">INPUTS</span></span>

### <span data-ttu-id="3ea95-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3ea95-136">System.String</span></span>

### <span data-ttu-id="3ea95-137">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3ea95-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="3ea95-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ea95-138">OUTPUTS</span></span>

### <span data-ttu-id="3ea95-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ea95-139">System.Boolean</span></span>

## <span data-ttu-id="3ea95-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ea95-140">NOTES</span></span>

## <span data-ttu-id="3ea95-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ea95-141">RELATED LINKS</span></span>
