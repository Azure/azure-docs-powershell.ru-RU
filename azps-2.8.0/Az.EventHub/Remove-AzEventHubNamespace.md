---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720933"
---
# <span data-ttu-id="42be6-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="42be6-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="42be6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42be6-102">SYNOPSIS</span></span>
<span data-ttu-id="42be6-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="42be6-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="42be6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42be6-104">SYNTAX</span></span>

### <span data-ttu-id="42be6-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42be6-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42be6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42be6-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42be6-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42be6-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42be6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42be6-108">DESCRIPTION</span></span>
<span data-ttu-id="42be6-109">Командлет Remove-AzEventHubNamespace удаляет и удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="42be6-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="42be6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42be6-110">EXAMPLES</span></span>

### <span data-ttu-id="42be6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42be6-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="42be6-112">Удаляет пространство имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="42be6-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="42be6-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="42be6-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="42be6-114">Пример 2,1-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="42be6-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="42be6-115">Пример 3,1-ResourceId-using Variable</span><span class="sxs-lookup"><span data-stu-id="42be6-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="42be6-116">Пример 3,2-ResourceId-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="42be6-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="42be6-117">Пример 3,3-ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="42be6-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="42be6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42be6-118">PARAMETERS</span></span>

### <span data-ttu-id="42be6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42be6-119">-AsJob</span></span>
<span data-ttu-id="42be6-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42be6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42be6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42be6-121">-DefaultProfile</span></span>
<span data-ttu-id="42be6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42be6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42be6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42be6-123">-InputObject</span></span>
<span data-ttu-id="42be6-124">Объект пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="42be6-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="42be6-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42be6-125">-Name</span></span>
<span data-ttu-id="42be6-126">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="42be6-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="42be6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42be6-127">-PassThru</span></span>
<span data-ttu-id="42be6-128">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="42be6-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="42be6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42be6-129">-ResourceGroupName</span></span>
<span data-ttu-id="42be6-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="42be6-130">Resource Group Name</span></span>

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

### <span data-ttu-id="42be6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42be6-131">-ResourceId</span></span>
<span data-ttu-id="42be6-132">Идентификатор ресурса пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="42be6-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="42be6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42be6-133">-Confirm</span></span>
<span data-ttu-id="42be6-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42be6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42be6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42be6-135">-WhatIf</span></span>
<span data-ttu-id="42be6-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42be6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42be6-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42be6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42be6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42be6-138">CommonParameters</span></span>
<span data-ttu-id="42be6-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42be6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42be6-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42be6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42be6-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42be6-141">INPUTS</span></span>

### <span data-ttu-id="42be6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="42be6-142">System.String</span></span>

### <span data-ttu-id="42be6-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="42be6-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="42be6-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42be6-144">OUTPUTS</span></span>

### <span data-ttu-id="42be6-145">System. void</span><span class="sxs-lookup"><span data-stu-id="42be6-145">System.Void</span></span>

## <span data-ttu-id="42be6-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="42be6-146">NOTES</span></span>

## <span data-ttu-id="42be6-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42be6-147">RELATED LINKS</span></span>
