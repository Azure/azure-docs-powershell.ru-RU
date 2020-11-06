---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: b8b2b9f6bb8a082647a14285a907465e8e12348f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565367"
---
# <span data-ttu-id="f4126-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="f4126-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="f4126-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4126-102">SYNOPSIS</span></span>
<span data-ttu-id="f4126-103">Удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f4126-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4126-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4126-104">SYNTAX</span></span>

### <span data-ttu-id="f4126-105">SubscriptionPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4126-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4126-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4126-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4126-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4126-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzureRmServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4126-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4126-108">DESCRIPTION</span></span>
<span data-ttu-id="f4126-109">Командлет **Remove-AzureRmServiceBusSubscription** удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f4126-109">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f4126-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4126-110">EXAMPLES</span></span>

### <span data-ttu-id="f4126-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4126-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="f4126-112">Удаляет подписку `SB-TopicSubscription-Example1` на раздел `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f4126-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f4126-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="f4126-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="f4126-114">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="f4126-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzureRmServiceBusSubscription <params> |Remove-AzureRmServiceBusSubscription
```

### <span data-ttu-id="f4126-115">Пример 3,1-ResourceId: использование переменной</span><span class="sxs-lookup"><span data-stu-id="f4126-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusSubscription <params>
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="f4126-116">Пример 3,2-ResourceId-использование строкового значения:</span><span class="sxs-lookup"><span data-stu-id="f4126-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="f4126-117">Удаляет подписку, указанную с помощью идентификатора ARM, в $resourceid/String для параметра-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4126-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="f4126-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4126-118">PARAMETERS</span></span>

### <span data-ttu-id="f4126-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4126-119">-AsJob</span></span>
<span data-ttu-id="f4126-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4126-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4126-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4126-121">-DefaultProfile</span></span>
<span data-ttu-id="f4126-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4126-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4126-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4126-123">-InputObject</span></span>
<span data-ttu-id="f4126-124">Объект подписки служебной шины</span><span class="sxs-lookup"><span data-stu-id="f4126-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="f4126-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4126-125">-Name</span></span>
<span data-ttu-id="f4126-126">Название подписки</span><span class="sxs-lookup"><span data-stu-id="f4126-126">Subscription Name</span></span>

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

### <span data-ttu-id="f4126-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4126-127">-Namespace</span></span>
<span data-ttu-id="f4126-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f4126-128">Namespace Name</span></span>

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

### <span data-ttu-id="f4126-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4126-129">-PassThru</span></span>
<span data-ttu-id="f4126-130">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f4126-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f4126-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4126-131">-ResourceGroupName</span></span>
<span data-ttu-id="f4126-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4126-132">The name of the resource group</span></span>

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

### <span data-ttu-id="f4126-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4126-133">-ResourceId</span></span>
<span data-ttu-id="f4126-134">Идентификатор ресурса подписки на обслуживание служебной шины</span><span class="sxs-lookup"><span data-stu-id="f4126-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="f4126-135">-Темы</span><span class="sxs-lookup"><span data-stu-id="f4126-135">-Topic</span></span>
<span data-ttu-id="f4126-136">Название раздела</span><span class="sxs-lookup"><span data-stu-id="f4126-136">Topic Name</span></span>

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

### <span data-ttu-id="f4126-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4126-137">-Confirm</span></span>
<span data-ttu-id="f4126-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4126-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4126-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4126-139">-WhatIf</span></span>
<span data-ttu-id="f4126-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4126-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4126-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4126-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4126-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4126-142">CommonParameters</span></span>
<span data-ttu-id="f4126-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4126-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4126-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4126-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4126-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4126-145">INPUTS</span></span>

### <span data-ttu-id="f4126-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f4126-146">System.String</span></span>

### <span data-ttu-id="f4126-147">Microsoft. Azure. Commands. ServiceBus. Models. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="f4126-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>
<span data-ttu-id="f4126-148">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4126-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f4126-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4126-149">OUTPUTS</span></span>

### <span data-ttu-id="f4126-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4126-150">System.Boolean</span></span>

## <span data-ttu-id="f4126-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4126-151">NOTES</span></span>

## <span data-ttu-id="f4126-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4126-152">RELATED LINKS</span></span>
