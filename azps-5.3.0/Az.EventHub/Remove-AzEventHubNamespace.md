---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507490"
---
# <span data-ttu-id="ace6a-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ace6a-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="ace6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ace6a-102">SYNOPSIS</span></span>
<span data-ttu-id="ace6a-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ace6a-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ace6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ace6a-104">SYNTAX</span></span>

### <span data-ttu-id="ace6a-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ace6a-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace6a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ace6a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ace6a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ace6a-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ace6a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ace6a-108">DESCRIPTION</span></span>
<span data-ttu-id="ace6a-109">Этот Remove-AzEventHubNamespace удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ace6a-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ace6a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ace6a-110">EXAMPLES</span></span>

### <span data-ttu-id="ace6a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ace6a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="ace6a-112">Удаляет пространство имен "Концентраторы \` событий" MyNamespaceName в группе ресурсов \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="ace6a-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ace6a-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="ace6a-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="ace6a-114">Пример 3. InputObject — использование piping:</span><span class="sxs-lookup"><span data-stu-id="ace6a-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="ace6a-115">Пример 4. ResourceId — использование переменной</span><span class="sxs-lookup"><span data-stu-id="ace6a-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="ace6a-116">Пример 5. ResourceId — использование piping:</span><span class="sxs-lookup"><span data-stu-id="ace6a-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="ace6a-117">Пример 6. ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="ace6a-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="ace6a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ace6a-118">PARAMETERS</span></span>

### <span data-ttu-id="ace6a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ace6a-119">-AsJob</span></span>
<span data-ttu-id="ace6a-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ace6a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ace6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace6a-121">-DefaultProfile</span></span>
<span data-ttu-id="ace6a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ace6a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ace6a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ace6a-123">-InputObject</span></span>
<span data-ttu-id="ace6a-124">Объект EventHubs Namespace</span><span class="sxs-lookup"><span data-stu-id="ace6a-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="ace6a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ace6a-125">-Name</span></span>
<span data-ttu-id="ace6a-126">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="ace6a-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="ace6a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ace6a-127">-PassThru</span></span>
<span data-ttu-id="ace6a-128">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="ace6a-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ace6a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ace6a-129">-ResourceGroupName</span></span>
<span data-ttu-id="ace6a-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ace6a-130">Resource Group Name</span></span>

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

### <span data-ttu-id="ace6a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ace6a-131">-ResourceId</span></span>
<span data-ttu-id="ace6a-132">EventHubs Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="ace6a-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="ace6a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ace6a-133">-Confirm</span></span>
<span data-ttu-id="ace6a-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ace6a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ace6a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ace6a-135">-WhatIf</span></span>
<span data-ttu-id="ace6a-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ace6a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ace6a-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ace6a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ace6a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace6a-138">CommonParameters</span></span>
<span data-ttu-id="ace6a-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ace6a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace6a-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace6a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace6a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ace6a-141">INPUTS</span></span>

### <span data-ttu-id="ace6a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ace6a-142">System.String</span></span>

### <span data-ttu-id="ace6a-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ace6a-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ace6a-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ace6a-144">OUTPUTS</span></span>

### <span data-ttu-id="ace6a-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="ace6a-145">System.Void</span></span>

## <span data-ttu-id="ace6a-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ace6a-146">NOTES</span></span>

## <span data-ttu-id="ace6a-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ace6a-147">RELATED LINKS</span></span>
