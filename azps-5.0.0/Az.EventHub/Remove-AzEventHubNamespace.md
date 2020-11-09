---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247446"
---
# <span data-ttu-id="85bcc-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="85bcc-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="85bcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="85bcc-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="85bcc-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="85bcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85bcc-104">SYNTAX</span></span>

### <span data-ttu-id="85bcc-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85bcc-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bcc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="85bcc-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85bcc-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85bcc-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85bcc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="85bcc-109">Командлет Remove-AzEventHubNamespace удаляет и удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="85bcc-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="85bcc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="85bcc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85bcc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="85bcc-112">Удаляет пространство имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="85bcc-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="85bcc-113">Пример 2: InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="85bcc-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="85bcc-114">Пример 3: InputObject — использование трубопроводов:</span><span class="sxs-lookup"><span data-stu-id="85bcc-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="85bcc-115">Пример 4: ResourceId — использование переменной</span><span class="sxs-lookup"><span data-stu-id="85bcc-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="85bcc-116">Пример 5: ResourceId — использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="85bcc-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="85bcc-117">Пример 6: ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="85bcc-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="85bcc-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85bcc-118">PARAMETERS</span></span>

### <span data-ttu-id="85bcc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85bcc-119">-AsJob</span></span>
<span data-ttu-id="85bcc-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="85bcc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85bcc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-121">-DefaultProfile</span></span>
<span data-ttu-id="85bcc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85bcc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85bcc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85bcc-123">-InputObject</span></span>
<span data-ttu-id="85bcc-124">Объект пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="85bcc-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="85bcc-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85bcc-125">-Name</span></span>
<span data-ttu-id="85bcc-126">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="85bcc-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="85bcc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85bcc-127">-PassThru</span></span>
<span data-ttu-id="85bcc-128">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="85bcc-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="85bcc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85bcc-129">-ResourceGroupName</span></span>
<span data-ttu-id="85bcc-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="85bcc-130">Resource Group Name</span></span>

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

### <span data-ttu-id="85bcc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85bcc-131">-ResourceId</span></span>
<span data-ttu-id="85bcc-132">Идентификатор ресурса пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="85bcc-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="85bcc-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85bcc-133">-Confirm</span></span>
<span data-ttu-id="85bcc-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85bcc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85bcc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85bcc-135">-WhatIf</span></span>
<span data-ttu-id="85bcc-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85bcc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85bcc-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85bcc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85bcc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bcc-138">CommonParameters</span></span>
<span data-ttu-id="85bcc-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85bcc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85bcc-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85bcc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bcc-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85bcc-141">INPUTS</span></span>

### <span data-ttu-id="85bcc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="85bcc-142">System.String</span></span>

### <span data-ttu-id="85bcc-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="85bcc-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="85bcc-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85bcc-144">OUTPUTS</span></span>

### <span data-ttu-id="85bcc-145">System. void</span><span class="sxs-lookup"><span data-stu-id="85bcc-145">System.Void</span></span>

## <span data-ttu-id="85bcc-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="85bcc-146">NOTES</span></span>

## <span data-ttu-id="85bcc-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85bcc-147">RELATED LINKS</span></span>