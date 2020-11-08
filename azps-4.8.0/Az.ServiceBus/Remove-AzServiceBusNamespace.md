---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243326"
---
# <span data-ttu-id="1af25-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1af25-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="1af25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1af25-102">SYNOPSIS</span></span>
<span data-ttu-id="1af25-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1af25-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="1af25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1af25-104">SYNTAX</span></span>

### <span data-ttu-id="1af25-105">NamespacePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1af25-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af25-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1af25-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1af25-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af25-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1af25-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af25-108">DESCRIPTION</span></span>
<span data-ttu-id="1af25-109">Командлет **Remove-AzServiceBusNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1af25-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="1af25-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1af25-110">EXAMPLES</span></span>

### <span data-ttu-id="1af25-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1af25-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="1af25-112">Удаляет пространство имен служебной шины `SB-Example1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="1af25-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="1af25-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="1af25-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="1af25-114">Удаляет пространство имен служебной шины, указанное в $inputobject.</span><span class="sxs-lookup"><span data-stu-id="1af25-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="1af25-115">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="1af25-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="1af25-116">Удаляет пространство имен служебной шины с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="1af25-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="1af25-117">Пример 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af25-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="1af25-118">Удаляет пространство имен служебной шины, указанное с помощью идентификатора ARM, в $resourceid для параметра-ResourceId или через конвейер.</span><span class="sxs-lookup"><span data-stu-id="1af25-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="1af25-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1af25-119">PARAMETERS</span></span>

### <span data-ttu-id="1af25-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1af25-120">-AsJob</span></span>
<span data-ttu-id="1af25-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1af25-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1af25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af25-122">-DefaultProfile</span></span>
<span data-ttu-id="1af25-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1af25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af25-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1af25-124">-InputObject</span></span>
<span data-ttu-id="1af25-125">Объект пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="1af25-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="1af25-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1af25-126">-Name</span></span>
<span data-ttu-id="1af25-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1af25-127">Namespace Name.</span></span>

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

### <span data-ttu-id="1af25-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1af25-128">-PassThru</span></span>
<span data-ttu-id="1af25-129">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1af25-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1af25-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af25-130">-ResourceGroupName</span></span>
<span data-ttu-id="1af25-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1af25-131">The name of the resource group</span></span>

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

### <span data-ttu-id="1af25-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af25-132">-ResourceId</span></span>
<span data-ttu-id="1af25-133">Идентификатор ресурса пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="1af25-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="1af25-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1af25-134">-Confirm</span></span>
<span data-ttu-id="1af25-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1af25-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1af25-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1af25-136">-WhatIf</span></span>
<span data-ttu-id="1af25-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1af25-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1af25-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1af25-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1af25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af25-139">CommonParameters</span></span>
<span data-ttu-id="1af25-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1af25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af25-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1af25-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af25-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1af25-142">INPUTS</span></span>

### <span data-ttu-id="1af25-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1af25-143">System.String</span></span>

### <span data-ttu-id="1af25-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1af25-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1af25-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1af25-145">OUTPUTS</span></span>

### <span data-ttu-id="1af25-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1af25-146">System.Boolean</span></span>

## <span data-ttu-id="1af25-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="1af25-147">NOTES</span></span>

## <span data-ttu-id="1af25-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1af25-148">RELATED LINKS</span></span>
