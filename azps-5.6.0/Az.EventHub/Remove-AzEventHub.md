---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 2d3f2ee9a4dc55dd709be3113770df402434c911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992785"
---
# <span data-ttu-id="fda7a-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="fda7a-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="fda7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fda7a-102">SYNOPSIS</span></span>
<span data-ttu-id="fda7a-103">Удаляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="fda7a-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="fda7a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fda7a-104">SYNTAX</span></span>

### <span data-ttu-id="fda7a-105">EventhubDefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fda7a-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda7a-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fda7a-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda7a-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda7a-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda7a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fda7a-108">DESCRIPTION</span></span>
<span data-ttu-id="fda7a-109">Этот Remove-AzEventHub удаляет указанный центр событий из указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fda7a-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="fda7a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fda7a-110">EXAMPLES</span></span>

### <span data-ttu-id="fda7a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fda7a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="fda7a-112">Удаляет Центр событий \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="fda7a-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="fda7a-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="fda7a-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="fda7a-114">Пример 3. InputObject с помощью piping:</span><span class="sxs-lookup"><span data-stu-id="fda7a-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="fda7a-115">Пример 4. ResourceId — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="fda7a-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="fda7a-116">Пример 5. ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="fda7a-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="fda7a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fda7a-117">PARAMETERS</span></span>

### <span data-ttu-id="fda7a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fda7a-118">-AsJob</span></span>
<span data-ttu-id="fda7a-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fda7a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fda7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda7a-120">-DefaultProfile</span></span>
<span data-ttu-id="fda7a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fda7a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda7a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fda7a-122">-InputObject</span></span>
<span data-ttu-id="fda7a-123">Объект Eventhub</span><span class="sxs-lookup"><span data-stu-id="fda7a-123">Eventhub Object</span></span>

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

### <span data-ttu-id="fda7a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fda7a-124">-Name</span></span>
<span data-ttu-id="fda7a-125">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="fda7a-125">EventHub Name</span></span>

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

### <span data-ttu-id="fda7a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fda7a-126">-Namespace</span></span>
<span data-ttu-id="fda7a-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="fda7a-127">Namespace Name</span></span>

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

### <span data-ttu-id="fda7a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fda7a-128">-PassThru</span></span>
<span data-ttu-id="fda7a-129">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="fda7a-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fda7a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda7a-130">-ResourceGroupName</span></span>
<span data-ttu-id="fda7a-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fda7a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="fda7a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fda7a-132">-ResourceId</span></span>
<span data-ttu-id="fda7a-133">ИД ресурса Вересюб</span><span class="sxs-lookup"><span data-stu-id="fda7a-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="fda7a-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fda7a-134">-Confirm</span></span>
<span data-ttu-id="fda7a-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda7a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda7a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda7a-136">-WhatIf</span></span>
<span data-ttu-id="fda7a-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fda7a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda7a-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fda7a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda7a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda7a-139">CommonParameters</span></span>
<span data-ttu-id="fda7a-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda7a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda7a-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda7a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda7a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fda7a-142">INPUTS</span></span>

### <span data-ttu-id="fda7a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="fda7a-143">System.String</span></span>

### <span data-ttu-id="fda7a-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="fda7a-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="fda7a-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fda7a-145">OUTPUTS</span></span>

### <span data-ttu-id="fda7a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fda7a-146">System.Boolean</span></span>

## <span data-ttu-id="fda7a-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fda7a-147">NOTES</span></span>

## <span data-ttu-id="fda7a-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fda7a-148">RELATED LINKS</span></span>
