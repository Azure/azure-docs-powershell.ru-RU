---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564552"
---
# <span data-ttu-id="ee925-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ee925-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="ee925-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee925-102">SYNOPSIS</span></span>
<span data-ttu-id="ee925-103">Удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ee925-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee925-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee925-104">SYNTAX</span></span>

### <span data-ttu-id="ee925-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee925-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee925-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee925-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee925-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee925-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee925-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee925-108">DESCRIPTION</span></span>
<span data-ttu-id="ee925-109">Командлет Remove-AzureRmEventHubNamespace удаляет и удаляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ee925-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ee925-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee925-110">EXAMPLES</span></span>

### <span data-ttu-id="ee925-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee925-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="ee925-112">Удаляет пространство имен MyNamespaceNameных концентраторов событий \` \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ee925-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ee925-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="ee925-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="ee925-114">Пример 2,1-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="ee925-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="ee925-115">Пример 3,1-ResourceId-using Variable</span><span class="sxs-lookup"><span data-stu-id="ee925-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="ee925-116">Пример 3,2-ResourceId-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="ee925-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="ee925-117">Пример 3,3-ResourceId — использование строки:</span><span class="sxs-lookup"><span data-stu-id="ee925-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="ee925-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee925-118">PARAMETERS</span></span>

### <span data-ttu-id="ee925-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee925-119">-AsJob</span></span>
<span data-ttu-id="ee925-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ee925-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee925-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee925-121">-DefaultProfile</span></span>
<span data-ttu-id="ee925-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee925-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee925-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee925-123">-InputObject</span></span>
<span data-ttu-id="ee925-124">Объект пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="ee925-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="ee925-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee925-125">-Name</span></span>
<span data-ttu-id="ee925-126">Имя пространства имен EventHub</span><span class="sxs-lookup"><span data-stu-id="ee925-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="ee925-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee925-127">-PassThru</span></span>
<span data-ttu-id="ee925-128">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ee925-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ee925-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee925-129">-ResourceGroupName</span></span>
<span data-ttu-id="ee925-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ee925-130">Resource Group Name</span></span>

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

### <span data-ttu-id="ee925-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee925-131">-ResourceId</span></span>
<span data-ttu-id="ee925-132">Идентификатор ресурса пространства имен EventHubs</span><span class="sxs-lookup"><span data-stu-id="ee925-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="ee925-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee925-133">-Confirm</span></span>
<span data-ttu-id="ee925-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee925-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee925-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee925-135">-WhatIf</span></span>
<span data-ttu-id="ee925-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee925-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee925-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee925-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee925-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee925-138">CommonParameters</span></span>
<span data-ttu-id="ee925-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee925-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee925-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee925-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee925-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee925-141">INPUTS</span></span>

### <span data-ttu-id="ee925-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ee925-142">System.String</span></span>

### <span data-ttu-id="ee925-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ee925-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="ee925-144">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee925-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ee925-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee925-145">OUTPUTS</span></span>

### <span data-ttu-id="ee925-146">System. void</span><span class="sxs-lookup"><span data-stu-id="ee925-146">System.Void</span></span>

## <span data-ttu-id="ee925-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee925-147">NOTES</span></span>

## <span data-ttu-id="ee925-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee925-148">RELATED LINKS</span></span>
