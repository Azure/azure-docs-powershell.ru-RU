---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: b17fa7309274f261c329eaf896519f8bb70d06fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905357"
---
# <span data-ttu-id="d19da-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d19da-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="d19da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d19da-102">SYNOPSIS</span></span>
<span data-ttu-id="d19da-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d19da-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="d19da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d19da-104">SYNTAX</span></span>

### <span data-ttu-id="d19da-105">NamespacePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d19da-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19da-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d19da-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d19da-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d19da-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19da-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d19da-108">DESCRIPTION</span></span>
<span data-ttu-id="d19da-109">Командлет **Remove-AzServiceBusNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d19da-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="d19da-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d19da-110">EXAMPLES</span></span>

### <span data-ttu-id="d19da-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d19da-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="d19da-112">Удаляет пространство имен служебной шины `SB-Example1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="d19da-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="d19da-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="d19da-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="d19da-114">Удаляет пространство имен служебной шины, указанное в $inputobject.</span><span class="sxs-lookup"><span data-stu-id="d19da-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="d19da-115">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="d19da-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="d19da-116">Удаляет пространство имен служебной шины с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d19da-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="d19da-117">Пример 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d19da-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="d19da-118">Удаляет пространство имен служебной шины, указанное с помощью идентификатора ARM, в $resourceid для параметра-ResourceId или через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d19da-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="d19da-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d19da-119">PARAMETERS</span></span>

### <span data-ttu-id="d19da-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d19da-120">-AsJob</span></span>
<span data-ttu-id="d19da-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d19da-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d19da-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19da-122">-DefaultProfile</span></span>
<span data-ttu-id="d19da-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d19da-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d19da-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d19da-124">-InputObject</span></span>
<span data-ttu-id="d19da-125">Объект пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="d19da-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="d19da-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d19da-126">-Name</span></span>
<span data-ttu-id="d19da-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d19da-127">Namespace Name.</span></span>

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

### <span data-ttu-id="d19da-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d19da-128">-PassThru</span></span>
<span data-ttu-id="d19da-129">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d19da-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d19da-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19da-130">-ResourceGroupName</span></span>
<span data-ttu-id="d19da-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d19da-131">The name of the resource group</span></span>

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

### <span data-ttu-id="d19da-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d19da-132">-ResourceId</span></span>
<span data-ttu-id="d19da-133">Идентификатор ресурса пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="d19da-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="d19da-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d19da-134">-Confirm</span></span>
<span data-ttu-id="d19da-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d19da-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19da-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19da-136">-WhatIf</span></span>
<span data-ttu-id="d19da-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d19da-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19da-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d19da-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19da-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19da-139">CommonParameters</span></span>
<span data-ttu-id="d19da-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d19da-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19da-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19da-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19da-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d19da-142">INPUTS</span></span>

### <span data-ttu-id="d19da-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d19da-143">System.String</span></span>

### <span data-ttu-id="d19da-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d19da-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d19da-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d19da-145">OUTPUTS</span></span>

### <span data-ttu-id="d19da-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d19da-146">System.Boolean</span></span>

## <span data-ttu-id="d19da-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d19da-147">NOTES</span></span>

## <span data-ttu-id="d19da-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d19da-148">RELATED LINKS</span></span>
