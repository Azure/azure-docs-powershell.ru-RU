---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 7f6a7225742356e0410d3cc49aef60e50e1954a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978104"
---
# <span data-ttu-id="da00b-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="da00b-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="da00b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da00b-102">SYNOPSIS</span></span>
<span data-ttu-id="da00b-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da00b-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="da00b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da00b-104">SYNTAX</span></span>

### <span data-ttu-id="da00b-105">NamespacePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da00b-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da00b-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="da00b-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da00b-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da00b-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da00b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da00b-108">DESCRIPTION</span></span>
<span data-ttu-id="da00b-109">Для **удаления пространства** имен из указанной группы ресурсов удаляется пространство имен.</span><span class="sxs-lookup"><span data-stu-id="da00b-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="da00b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da00b-110">EXAMPLES</span></span>

### <span data-ttu-id="da00b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da00b-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="da00b-112">Удаляет пространство имен "Автобус обслуживания" из указанной группы `SB-Example1` `Default-ServiceBus-WestUS` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da00b-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="da00b-113">Пример 2.1 — InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="da00b-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="da00b-114">Удаляет пространство имен автобусов обслуживания, предоставленное через $inputobject.</span><span class="sxs-lookup"><span data-stu-id="da00b-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="da00b-115">Пример 2.2 . InputObject - Использование piping:</span><span class="sxs-lookup"><span data-stu-id="da00b-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="da00b-116">Удаляет пространство имен автобусов обслуживания с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="da00b-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="da00b-117">Пример 3. ResourceId</span><span class="sxs-lookup"><span data-stu-id="da00b-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="da00b-118">Удаляет пространство имен автобусов обслуживания, предоставленное ARM в $resourceid параметра -ResourceId или путем piping.</span><span class="sxs-lookup"><span data-stu-id="da00b-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="da00b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da00b-119">PARAMETERS</span></span>

### <span data-ttu-id="da00b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da00b-120">-AsJob</span></span>
<span data-ttu-id="da00b-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="da00b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da00b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da00b-122">-DefaultProfile</span></span>
<span data-ttu-id="da00b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da00b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da00b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da00b-124">-InputObject</span></span>
<span data-ttu-id="da00b-125">Объект Namespace для автобусов обслуживания</span><span class="sxs-lookup"><span data-stu-id="da00b-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da00b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="da00b-126">-Name</span></span>
<span data-ttu-id="da00b-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="da00b-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da00b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da00b-128">-PassThru</span></span>
<span data-ttu-id="da00b-129">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="da00b-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="da00b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da00b-130">-ResourceGroupName</span></span>
<span data-ttu-id="da00b-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="da00b-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da00b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da00b-132">-ResourceId</span></span>
<span data-ttu-id="da00b-133">Service Bus Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="da00b-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="da00b-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da00b-134">-Confirm</span></span>
<span data-ttu-id="da00b-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="da00b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da00b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da00b-136">-WhatIf</span></span>
<span data-ttu-id="da00b-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da00b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da00b-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da00b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da00b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da00b-139">CommonParameters</span></span>
<span data-ttu-id="da00b-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da00b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da00b-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da00b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da00b-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da00b-142">INPUTS</span></span>

### <span data-ttu-id="da00b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="da00b-143">System.String</span></span>

### <span data-ttu-id="da00b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="da00b-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="da00b-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da00b-145">OUTPUTS</span></span>

### <span data-ttu-id="da00b-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da00b-146">System.Boolean</span></span>

## <span data-ttu-id="da00b-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da00b-147">NOTES</span></span>

## <span data-ttu-id="da00b-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da00b-148">RELATED LINKS</span></span>
