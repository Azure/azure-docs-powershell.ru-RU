---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566459"
---
# <span data-ttu-id="3c5d4-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="3c5d4-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="3c5d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c5d4-103">Удаляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c5d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c5d4-104">SYNTAX</span></span>

### <span data-ttu-id="3c5d4-105">EventhubDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c5d4-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c5d4-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3c5d4-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c5d4-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c5d4-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c5d4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c5d4-108">DESCRIPTION</span></span>
<span data-ttu-id="3c5d4-109">Командлет Remove-AzureRmEventHub удаляет и удаляет указанный концентратор событий из заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="3c5d4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c5d4-110">EXAMPLES</span></span>

### <span data-ttu-id="3c5d4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c5d4-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="3c5d4-112">Удаляет MyEventHubName концентратора \` событий \` .</span><span class="sxs-lookup"><span data-stu-id="3c5d4-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="3c5d4-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="3c5d4-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="3c5d4-114">Пример 2,2-InputObject с использованием конвейера:</span><span class="sxs-lookup"><span data-stu-id="3c5d4-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="3c5d4-115">Пример 3,1-ResourceId: использование переменной</span><span class="sxs-lookup"><span data-stu-id="3c5d4-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="3c5d4-116">Пример 3,1-ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="3c5d4-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="3c5d4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c5d4-117">PARAMETERS</span></span>

### <span data-ttu-id="3c5d4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c5d4-118">-AsJob</span></span>
<span data-ttu-id="3c5d4-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3c5d4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c5d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c5d4-120">-DefaultProfile</span></span>
<span data-ttu-id="3c5d4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c5d4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c5d4-122">-InputObject</span></span>
<span data-ttu-id="3c5d4-123">Объект Eventhub</span><span class="sxs-lookup"><span data-stu-id="3c5d4-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c5d4-124">-Name</span></span>
<span data-ttu-id="3c5d4-125">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="3c5d4-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3c5d4-126">-Namespace</span></span>
<span data-ttu-id="3c5d4-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="3c5d4-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c5d4-128">-PassThru</span></span>
<span data-ttu-id="3c5d4-129">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3c5d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c5d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="3c5d4-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3c5d4-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c5d4-132">-ResourceId</span></span>
<span data-ttu-id="3c5d4-133">Идентификатор ресурса Eventhub</span><span class="sxs-lookup"><span data-stu-id="3c5d4-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c5d4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c5d4-134">-Confirm</span></span>
<span data-ttu-id="3c5d4-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c5d4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c5d4-136">-WhatIf</span></span>
<span data-ttu-id="3c5d4-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c5d4-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c5d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c5d4-139">CommonParameters</span></span>
<span data-ttu-id="3c5d4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c5d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c5d4-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c5d4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c5d4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c5d4-142">INPUTS</span></span>

### <span data-ttu-id="3c5d4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3c5d4-143">System.String</span></span>

### <span data-ttu-id="3c5d4-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3c5d4-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="3c5d4-145">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3c5d4-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3c5d4-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c5d4-146">OUTPUTS</span></span>

### <span data-ttu-id="3c5d4-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c5d4-147">System.Boolean</span></span>

## <span data-ttu-id="3c5d4-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c5d4-148">NOTES</span></span>

## <span data-ttu-id="3c5d4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c5d4-149">RELATED LINKS</span></span>
