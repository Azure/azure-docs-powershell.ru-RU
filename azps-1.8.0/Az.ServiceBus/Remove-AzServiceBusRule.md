---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: 711213f7bb647d505d02b5492a9d9eb619959a5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729160"
---
# <span data-ttu-id="2dee9-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="2dee9-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="2dee9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dee9-102">SYNOPSIS</span></span>
<span data-ttu-id="2dee9-103">Удаляет правило speficied для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="2dee9-103">Removes the speficied rule of a given subscription .</span></span>

## <span data-ttu-id="2dee9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dee9-104">SYNTAX</span></span>

### <span data-ttu-id="2dee9-105">RulePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2dee9-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dee9-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2dee9-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dee9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dee9-107">DESCRIPTION</span></span>
<span data-ttu-id="2dee9-108">Командлет **Remove-AzServiceBusRule** удаляет правило подписки на данную тему.</span><span class="sxs-lookup"><span data-stu-id="2dee9-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="2dee9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dee9-109">EXAMPLES</span></span>

### <span data-ttu-id="2dee9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2dee9-110">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="2dee9-111">Удаляет правило `SBRule` подписки `SBSubscription` для указанной темы `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="2dee9-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="2dee9-112">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="2dee9-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="2dee9-113">Удаляет правило, указанное в параметре $inputobject для параметра-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dee9-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="2dee9-114">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="2dee9-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="2dee9-115">Пример 3,1-ResourceId-using Variable</span><span class="sxs-lookup"><span data-stu-id="2dee9-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="2dee9-116">Пример 3,1-ResourceId-использование строкового значения</span><span class="sxs-lookup"><span data-stu-id="2dee9-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="2dee9-117">Удаляет правило, указанное с помощью идентификатора ARM, в $resourceid/String для-ResourceId (параметр)</span><span class="sxs-lookup"><span data-stu-id="2dee9-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="2dee9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dee9-118">PARAMETERS</span></span>

### <span data-ttu-id="2dee9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dee9-119">-AsJob</span></span>
<span data-ttu-id="2dee9-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2dee9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dee9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dee9-121">-DefaultProfile</span></span>
<span data-ttu-id="2dee9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dee9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dee9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2dee9-123">-Force</span></span>
<span data-ttu-id="2dee9-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2dee9-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2dee9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dee9-125">-InputObject</span></span>
<span data-ttu-id="2dee9-126">Объект правила служебной шины</span><span class="sxs-lookup"><span data-stu-id="2dee9-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2dee9-127">-Name</span></span>
<span data-ttu-id="2dee9-128">Имя правила</span><span class="sxs-lookup"><span data-stu-id="2dee9-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2dee9-129">-Namespace</span></span>
<span data-ttu-id="2dee9-130">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2dee9-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dee9-131">-PassThru</span></span>
<span data-ttu-id="2dee9-132">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2dee9-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2dee9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dee9-133">-ResourceGroupName</span></span>
<span data-ttu-id="2dee9-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2dee9-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dee9-135">-ResourceId</span></span>
<span data-ttu-id="2dee9-136">Идентификатор ресурса правила служебной шины</span><span class="sxs-lookup"><span data-stu-id="2dee9-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-137">-Подписка</span><span class="sxs-lookup"><span data-stu-id="2dee9-137">-Subscription</span></span>
<span data-ttu-id="2dee9-138">Название подписки</span><span class="sxs-lookup"><span data-stu-id="2dee9-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-139">-Темы</span><span class="sxs-lookup"><span data-stu-id="2dee9-139">-Topic</span></span>
<span data-ttu-id="2dee9-140">Название раздела</span><span class="sxs-lookup"><span data-stu-id="2dee9-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dee9-141">-Confirm</span></span>
<span data-ttu-id="2dee9-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2dee9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dee9-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dee9-143">-WhatIf</span></span>
<span data-ttu-id="2dee9-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2dee9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dee9-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2dee9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dee9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dee9-146">CommonParameters</span></span>
<span data-ttu-id="2dee9-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dee9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dee9-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dee9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dee9-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dee9-149">INPUTS</span></span>

### <span data-ttu-id="2dee9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2dee9-150">System.String</span></span>

### <span data-ttu-id="2dee9-151">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="2dee9-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="2dee9-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dee9-152">OUTPUTS</span></span>

### <span data-ttu-id="2dee9-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2dee9-153">System.Boolean</span></span>

## <span data-ttu-id="2dee9-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dee9-154">NOTES</span></span>

## <span data-ttu-id="2dee9-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dee9-155">RELATED LINKS</span></span>
