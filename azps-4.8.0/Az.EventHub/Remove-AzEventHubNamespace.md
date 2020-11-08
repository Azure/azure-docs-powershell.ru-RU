---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242782"
---
# <span data-ttu-id="b2fe8-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b2fe8-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="b2fe8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="b2fe8-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b2fe8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2fe8-104">SYNTAX</span></span>

### <span data-ttu-id="b2fe8-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2fe8-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2fe8-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b2fe8-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2fe8-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2fe8-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2fe8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2fe8-108">DESCRIPTION</span></span>
<span data-ttu-id="b2fe8-109">Командлет Remove-AzEventHubNamespace удаляет и удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="b2fe8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2fe8-110">EXAMPLES</span></span>

### <span data-ttu-id="b2fe8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2fe8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="b2fe8-112">Удаляет пространство имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b2fe8-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b2fe8-113">Пример 2: InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="b2fe8-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="b2fe8-114">Пример 3: InputObject — использование трубопроводов:</span><span class="sxs-lookup"><span data-stu-id="b2fe8-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="b2fe8-115">Пример 4: ResourceId — использование переменной</span><span class="sxs-lookup"><span data-stu-id="b2fe8-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="b2fe8-116">Пример 5: ResourceId — использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="b2fe8-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="b2fe8-117">Пример 6: ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="b2fe8-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="b2fe8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2fe8-118">PARAMETERS</span></span>

### <span data-ttu-id="b2fe8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2fe8-119">-AsJob</span></span>
<span data-ttu-id="b2fe8-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b2fe8-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2fe8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2fe8-121">-DefaultProfile</span></span>
<span data-ttu-id="b2fe8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2fe8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2fe8-123">-InputObject</span></span>
<span data-ttu-id="b2fe8-124">Объект пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="b2fe8-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2fe8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2fe8-125">-Name</span></span>
<span data-ttu-id="b2fe8-126">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="b2fe8-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2fe8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2fe8-127">-PassThru</span></span>
<span data-ttu-id="b2fe8-128">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b2fe8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2fe8-129">-ResourceGroupName</span></span>
<span data-ttu-id="b2fe8-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2fe8-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2fe8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2fe8-131">-ResourceId</span></span>
<span data-ttu-id="b2fe8-132">Идентификатор ресурса пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="b2fe8-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2fe8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2fe8-133">-Confirm</span></span>
<span data-ttu-id="b2fe8-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2fe8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2fe8-135">-WhatIf</span></span>
<span data-ttu-id="b2fe8-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2fe8-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2fe8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2fe8-138">CommonParameters</span></span>
<span data-ttu-id="b2fe8-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2fe8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2fe8-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2fe8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2fe8-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2fe8-141">INPUTS</span></span>

### <span data-ttu-id="b2fe8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b2fe8-142">System.String</span></span>

### <span data-ttu-id="b2fe8-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b2fe8-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="b2fe8-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2fe8-144">OUTPUTS</span></span>

### <span data-ttu-id="b2fe8-145">System. void</span><span class="sxs-lookup"><span data-stu-id="b2fe8-145">System.Void</span></span>

## <span data-ttu-id="b2fe8-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2fe8-146">NOTES</span></span>

## <span data-ttu-id="b2fe8-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2fe8-147">RELATED LINKS</span></span>
