---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0369d6bac19d2d2180c54f3c4244101df3a7bb42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903810"
---
# <span data-ttu-id="f5674-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="f5674-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="f5674-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5674-102">SYNOPSIS</span></span>
<span data-ttu-id="f5674-103">Удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f5674-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f5674-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5674-104">SYNTAX</span></span>

### <span data-ttu-id="f5674-105">SubscriptionPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5674-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5674-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5674-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5674-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5674-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5674-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5674-108">DESCRIPTION</span></span>
<span data-ttu-id="f5674-109">Командлет **Remove-AzServiceBusSubscription** удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f5674-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f5674-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5674-110">EXAMPLES</span></span>

### <span data-ttu-id="f5674-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5674-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="f5674-112">Удаляет подписку `SB-TopicSubscription-Example1` на раздел `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f5674-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f5674-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="f5674-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="f5674-114">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="f5674-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="f5674-115">Пример 3,1-ResourceId: использование переменной</span><span class="sxs-lookup"><span data-stu-id="f5674-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="f5674-116">Пример 3,2-ResourceId-использование строкового значения:</span><span class="sxs-lookup"><span data-stu-id="f5674-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="f5674-117">Удаляет подписку, указанную с помощью идентификатора ARM, в $resourceid/String для параметра-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5674-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="f5674-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5674-118">PARAMETERS</span></span>

### <span data-ttu-id="f5674-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5674-119">-AsJob</span></span>
<span data-ttu-id="f5674-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f5674-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5674-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5674-121">-DefaultProfile</span></span>
<span data-ttu-id="f5674-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5674-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5674-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5674-123">-InputObject</span></span>
<span data-ttu-id="f5674-124">Объект подписки служебной шины</span><span class="sxs-lookup"><span data-stu-id="f5674-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5674-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5674-125">-Name</span></span>
<span data-ttu-id="f5674-126">Название подписки</span><span class="sxs-lookup"><span data-stu-id="f5674-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5674-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5674-127">-Namespace</span></span>
<span data-ttu-id="f5674-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f5674-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5674-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5674-129">-PassThru</span></span>
<span data-ttu-id="f5674-130">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f5674-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f5674-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5674-131">-ResourceGroupName</span></span>
<span data-ttu-id="f5674-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5674-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5674-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5674-133">-ResourceId</span></span>
<span data-ttu-id="f5674-134">Идентификатор ресурса подписки на обслуживание служебной шины</span><span class="sxs-lookup"><span data-stu-id="f5674-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5674-135">-Темы</span><span class="sxs-lookup"><span data-stu-id="f5674-135">-Topic</span></span>
<span data-ttu-id="f5674-136">Название раздела</span><span class="sxs-lookup"><span data-stu-id="f5674-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5674-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5674-137">-Confirm</span></span>
<span data-ttu-id="f5674-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5674-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5674-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5674-139">-WhatIf</span></span>
<span data-ttu-id="f5674-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5674-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5674-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5674-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5674-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5674-142">CommonParameters</span></span>
<span data-ttu-id="f5674-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5674-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5674-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5674-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5674-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5674-145">INPUTS</span></span>

### <span data-ttu-id="f5674-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f5674-146">System.String</span></span>

### <span data-ttu-id="f5674-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="f5674-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="f5674-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5674-148">OUTPUTS</span></span>

### <span data-ttu-id="f5674-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5674-149">System.Boolean</span></span>

## <span data-ttu-id="f5674-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5674-150">NOTES</span></span>

## <span data-ttu-id="f5674-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5674-151">RELATED LINKS</span></span>
