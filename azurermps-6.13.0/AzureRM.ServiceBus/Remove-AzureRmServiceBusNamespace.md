---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732447"
---
# <span data-ttu-id="b8de0-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="b8de0-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="b8de0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8de0-102">SYNOPSIS</span></span>
<span data-ttu-id="b8de0-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8de0-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8de0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8de0-104">SYNTAX</span></span>

### <span data-ttu-id="b8de0-105">NamespacePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8de0-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8de0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8de0-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8de0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8de0-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8de0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8de0-108">DESCRIPTION</span></span>
<span data-ttu-id="b8de0-109">Командлет **Remove-AzureRmServiceBusNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8de0-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="b8de0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8de0-110">EXAMPLES</span></span>

### <span data-ttu-id="b8de0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8de0-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="b8de0-112">Удаляет пространство имен служебной шины `SB-Example1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="b8de0-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="b8de0-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="b8de0-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="b8de0-114">Удаляет пространство имен служебной шины, указанное в $inputobject.</span><span class="sxs-lookup"><span data-stu-id="b8de0-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="b8de0-115">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="b8de0-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="b8de0-116">Удаляет пространство имен служебной шины с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="b8de0-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="b8de0-117">Пример 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8de0-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="b8de0-118">Удаляет пространство имен служебной шины, указанное с помощью идентификатора ARM, в $resourceid для параметра-ResourceId или через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b8de0-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="b8de0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8de0-119">PARAMETERS</span></span>

### <span data-ttu-id="b8de0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8de0-120">-AsJob</span></span>
<span data-ttu-id="b8de0-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b8de0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8de0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8de0-122">-DefaultProfile</span></span>
<span data-ttu-id="b8de0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8de0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8de0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8de0-124">-InputObject</span></span>
<span data-ttu-id="b8de0-125">Объект пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="b8de0-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="b8de0-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8de0-126">-Name</span></span>
<span data-ttu-id="b8de0-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b8de0-127">Namespace Name.</span></span>

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

### <span data-ttu-id="b8de0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8de0-128">-PassThru</span></span>
<span data-ttu-id="b8de0-129">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b8de0-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b8de0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8de0-130">-ResourceGroupName</span></span>
<span data-ttu-id="b8de0-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8de0-131">The name of the resource group</span></span>

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

### <span data-ttu-id="b8de0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8de0-132">-ResourceId</span></span>
<span data-ttu-id="b8de0-133">Идентификатор ресурса пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="b8de0-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="b8de0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8de0-134">-Confirm</span></span>
<span data-ttu-id="b8de0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8de0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8de0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8de0-136">-WhatIf</span></span>
<span data-ttu-id="b8de0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8de0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8de0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8de0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8de0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8de0-139">CommonParameters</span></span>
<span data-ttu-id="b8de0-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8de0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8de0-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8de0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8de0-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8de0-142">INPUTS</span></span>

### <span data-ttu-id="b8de0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b8de0-143">System.String</span></span>

### <span data-ttu-id="b8de0-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="b8de0-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="b8de0-145">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8de0-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b8de0-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8de0-146">OUTPUTS</span></span>

### <span data-ttu-id="b8de0-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b8de0-147">System.Boolean</span></span>

## <span data-ttu-id="b8de0-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8de0-148">NOTES</span></span>

## <span data-ttu-id="b8de0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8de0-149">RELATED LINKS</span></span>
