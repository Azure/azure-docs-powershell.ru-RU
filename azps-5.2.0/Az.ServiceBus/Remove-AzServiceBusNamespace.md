---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417516"
---
# <span data-ttu-id="f2fbb-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f2fbb-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="f2fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fbb-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="f2fbb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2fbb-104">SYNTAX</span></span>

### <span data-ttu-id="f2fbb-105">NamespacePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2fbb-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fbb-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2fbb-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fbb-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2fbb-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2fbb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2fbb-108">DESCRIPTION</span></span>
<span data-ttu-id="f2fbb-109">Для **удаления пространства** имен из указанной группы ресурсов удаляется пространство имен.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="f2fbb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2fbb-110">EXAMPLES</span></span>

### <span data-ttu-id="f2fbb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2fbb-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="f2fbb-112">Удаляет пространство имен автобусов обслуживания из указанной группы `SB-Example1` `Default-ServiceBus-WestUS` ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="f2fbb-113">Пример 2.1 — InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="f2fbb-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="f2fbb-114">Удаляет пространство имен автобусов обслуживания, предоставленное через $inputobject.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="f2fbb-115">Пример 2.2 . InputObject - Использование piping:</span><span class="sxs-lookup"><span data-stu-id="f2fbb-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="f2fbb-116">Удаляет пространство имен автобусов обслуживания с помощью Piping.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="f2fbb-117">Пример 3. ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2fbb-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="f2fbb-118">Удаляет пространство имен автобусов обслуживания, предоставленное ARM в $resourceid параметра -ResourceId или путем piping.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="f2fbb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2fbb-119">PARAMETERS</span></span>

### <span data-ttu-id="f2fbb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2fbb-120">-AsJob</span></span>
<span data-ttu-id="f2fbb-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f2fbb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2fbb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fbb-122">-DefaultProfile</span></span>
<span data-ttu-id="f2fbb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2fbb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2fbb-124">-InputObject</span></span>
<span data-ttu-id="f2fbb-125">Объект Namespace для автобусов обслуживания</span><span class="sxs-lookup"><span data-stu-id="f2fbb-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="f2fbb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f2fbb-126">-Name</span></span>
<span data-ttu-id="f2fbb-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-127">Namespace Name.</span></span>

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

### <span data-ttu-id="f2fbb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2fbb-128">-PassThru</span></span>
<span data-ttu-id="f2fbb-129">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f2fbb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fbb-130">-ResourceGroupName</span></span>
<span data-ttu-id="f2fbb-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f2fbb-131">The name of the resource group</span></span>

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

### <span data-ttu-id="f2fbb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2fbb-132">-ResourceId</span></span>
<span data-ttu-id="f2fbb-133">Service Bus Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="f2fbb-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="f2fbb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2fbb-134">-Confirm</span></span>
<span data-ttu-id="f2fbb-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2fbb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2fbb-136">-WhatIf</span></span>
<span data-ttu-id="f2fbb-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2fbb-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2fbb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fbb-139">CommonParameters</span></span>
<span data-ttu-id="f2fbb-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2fbb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fbb-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2fbb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fbb-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2fbb-142">INPUTS</span></span>

### <span data-ttu-id="f2fbb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f2fbb-143">System.String</span></span>

### <span data-ttu-id="f2fbb-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f2fbb-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f2fbb-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2fbb-145">OUTPUTS</span></span>

### <span data-ttu-id="f2fbb-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2fbb-146">System.Boolean</span></span>

## <span data-ttu-id="f2fbb-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2fbb-147">NOTES</span></span>

## <span data-ttu-id="f2fbb-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2fbb-148">RELATED LINKS</span></span>
