---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426175"
---
# <span data-ttu-id="1fd0d-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="1fd0d-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="1fd0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="1fd0d-103">Удаляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="1fd0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1fd0d-104">SYNTAX</span></span>

### <span data-ttu-id="1fd0d-105">EventhubDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fd0d-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fd0d-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1fd0d-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fd0d-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fd0d-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fd0d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fd0d-108">DESCRIPTION</span></span>
<span data-ttu-id="1fd0d-109">Этот Remove-AzEventHub удаляет указанный центр событий из указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="1fd0d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1fd0d-110">EXAMPLES</span></span>

### <span data-ttu-id="1fd0d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fd0d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="1fd0d-112">Удаляет Центр событий \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="1fd0d-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="1fd0d-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="1fd0d-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="1fd0d-114">Пример 3. InputObject с помощью piping:</span><span class="sxs-lookup"><span data-stu-id="1fd0d-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="1fd0d-115">Пример 4. ResourceId — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="1fd0d-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="1fd0d-116">Пример 5. ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="1fd0d-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="1fd0d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fd0d-117">PARAMETERS</span></span>

### <span data-ttu-id="1fd0d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fd0d-118">-AsJob</span></span>
<span data-ttu-id="1fd0d-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1fd0d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fd0d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fd0d-120">-DefaultProfile</span></span>
<span data-ttu-id="1fd0d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fd0d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fd0d-122">-InputObject</span></span>
<span data-ttu-id="1fd0d-123">Объект Eventhub</span><span class="sxs-lookup"><span data-stu-id="1fd0d-123">Eventhub Object</span></span>

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

### <span data-ttu-id="1fd0d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1fd0d-124">-Name</span></span>
<span data-ttu-id="1fd0d-125">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="1fd0d-125">EventHub Name</span></span>

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

### <span data-ttu-id="1fd0d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1fd0d-126">-Namespace</span></span>
<span data-ttu-id="1fd0d-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="1fd0d-127">Namespace Name</span></span>

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

### <span data-ttu-id="1fd0d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fd0d-128">-PassThru</span></span>
<span data-ttu-id="1fd0d-129">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1fd0d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fd0d-130">-ResourceGroupName</span></span>
<span data-ttu-id="1fd0d-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1fd0d-131">Resource Group Name</span></span>

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

### <span data-ttu-id="1fd0d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fd0d-132">-ResourceId</span></span>
<span data-ttu-id="1fd0d-133">ИД ресурса Вересюб</span><span class="sxs-lookup"><span data-stu-id="1fd0d-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="1fd0d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fd0d-134">-Confirm</span></span>
<span data-ttu-id="1fd0d-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fd0d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fd0d-136">-WhatIf</span></span>
<span data-ttu-id="1fd0d-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fd0d-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fd0d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fd0d-139">CommonParameters</span></span>
<span data-ttu-id="1fd0d-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fd0d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fd0d-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fd0d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fd0d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fd0d-142">INPUTS</span></span>

### <span data-ttu-id="1fd0d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1fd0d-143">System.String</span></span>

### <span data-ttu-id="1fd0d-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="1fd0d-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="1fd0d-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1fd0d-145">OUTPUTS</span></span>

### <span data-ttu-id="1fd0d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1fd0d-146">System.Boolean</span></span>

## <span data-ttu-id="1fd0d-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1fd0d-147">NOTES</span></span>

## <span data-ttu-id="1fd0d-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fd0d-148">RELATED LINKS</span></span>
