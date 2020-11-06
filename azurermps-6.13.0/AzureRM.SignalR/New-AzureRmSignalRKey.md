---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalRKey.md
ms.openlocfilehash: 4b4f3a416ece999641570a33101a3e7ab201ca3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565344"
---
# <span data-ttu-id="f2b82-101">New-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="f2b82-101">New-AzureRmSignalRKey</span></span>

## <span data-ttu-id="f2b82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2b82-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b82-103">Повторное создание клавиши доступа для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="f2b82-103">Regenerate an access key for a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2b82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2b82-104">SYNTAX</span></span>

### <span data-ttu-id="f2b82-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2b82-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b82-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2b82-106">ResourceIdParameterSet</span></span>
```
New-AzureRmSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2b82-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2b82-107">InputObjectParameterSet</span></span>
```
New-AzureRmSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b82-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2b82-108">DESCRIPTION</span></span>
<span data-ttu-id="f2b82-109">Повторное создание клавиши доступа для службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="f2b82-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f2b82-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2b82-110">EXAMPLES</span></span>

### <span data-ttu-id="f2b82-111">Повторное создание первичного ключа</span><span class="sxs-lookup"><span data-stu-id="f2b82-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="f2b82-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2b82-112">PARAMETERS</span></span>

### <span data-ttu-id="f2b82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b82-113">-DefaultProfile</span></span>
<span data-ttu-id="f2b82-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b82-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2b82-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2b82-115">-InputObject</span></span>
<span data-ttu-id="f2b82-116">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="f2b82-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f2b82-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f2b82-117">-KeyType</span></span>
<span data-ttu-id="f2b82-118">Тип ключа: Primary или Secondary.</span><span class="sxs-lookup"><span data-stu-id="f2b82-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="f2b82-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2b82-119">-Name</span></span>
<span data-ttu-id="f2b82-120">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="f2b82-120">SignalR service name.</span></span>

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

### <span data-ttu-id="f2b82-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2b82-121">-PassThru</span></span>
<span data-ttu-id="f2b82-122">Возвращает значение "истина", если повторное создание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="f2b82-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="f2b82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2b82-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2b82-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2b82-124">Resource group name.</span></span>

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

### <span data-ttu-id="f2b82-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2b82-125">-ResourceId</span></span>
<span data-ttu-id="f2b82-126">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="f2b82-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f2b82-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2b82-127">-Confirm</span></span>
<span data-ttu-id="f2b82-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2b82-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2b82-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b82-129">-WhatIf</span></span>
<span data-ttu-id="f2b82-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2b82-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b82-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2b82-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2b82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b82-132">CommonParameters</span></span>
<span data-ttu-id="f2b82-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2b82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b82-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b82-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b82-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2b82-135">INPUTS</span></span>

### <span data-ttu-id="f2b82-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f2b82-136">System.String</span></span>
<span data-ttu-id="f2b82-137">Параметры: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2b82-137">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="f2b82-138">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="f2b82-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="f2b82-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f2b82-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f2b82-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2b82-140">OUTPUTS</span></span>

### <span data-ttu-id="f2b82-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2b82-141">System.Boolean</span></span>

## <span data-ttu-id="f2b82-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2b82-142">NOTES</span></span>

## <span data-ttu-id="f2b82-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2b82-143">RELATED LINKS</span></span>
