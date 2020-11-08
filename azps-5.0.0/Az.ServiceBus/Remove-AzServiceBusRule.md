---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245255"
---
# <span data-ttu-id="e933d-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="e933d-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="e933d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e933d-102">SYNOPSIS</span></span>
<span data-ttu-id="e933d-103">Удаляет указанное правило данной подписки.</span><span class="sxs-lookup"><span data-stu-id="e933d-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="e933d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e933d-104">SYNTAX</span></span>

### <span data-ttu-id="e933d-105">RulePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e933d-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e933d-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e933d-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e933d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e933d-107">DESCRIPTION</span></span>
<span data-ttu-id="e933d-108">Командлет **Remove-AzServiceBusRule** удаляет правило подписки на данную тему.</span><span class="sxs-lookup"><span data-stu-id="e933d-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="e933d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e933d-109">EXAMPLES</span></span>

### <span data-ttu-id="e933d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e933d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="e933d-111">Удаляет правило `SBRule` подписки `SBSubscription` для указанной темы `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="e933d-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="e933d-112">Пример 2: InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="e933d-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="e933d-113">Удаляет правило, указанное в параметре $inputobject для параметра-InputObject</span><span class="sxs-lookup"><span data-stu-id="e933d-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="e933d-114">Пример 3: InputObject — использование трубопроводов:</span><span class="sxs-lookup"><span data-stu-id="e933d-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="e933d-115">Пример 4: ResourceId — использование переменной</span><span class="sxs-lookup"><span data-stu-id="e933d-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="e933d-116">Пример 5: ResourceId — использование строкового значения</span><span class="sxs-lookup"><span data-stu-id="e933d-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="e933d-117">Удаляет правило, указанное с помощью идентификатора ARM, в $resourceid/String для-ResourceId (параметр)</span><span class="sxs-lookup"><span data-stu-id="e933d-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="e933d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e933d-118">PARAMETERS</span></span>

### <span data-ttu-id="e933d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e933d-119">-AsJob</span></span>
<span data-ttu-id="e933d-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e933d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e933d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e933d-121">-DefaultProfile</span></span>
<span data-ttu-id="e933d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e933d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e933d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e933d-123">-Force</span></span>
<span data-ttu-id="e933d-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e933d-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e933d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e933d-125">-InputObject</span></span>
<span data-ttu-id="e933d-126">Объект правила служебной шины</span><span class="sxs-lookup"><span data-stu-id="e933d-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="e933d-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e933d-127">-Name</span></span>
<span data-ttu-id="e933d-128">Имя правила</span><span class="sxs-lookup"><span data-stu-id="e933d-128">Rule Name</span></span>

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

### <span data-ttu-id="e933d-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e933d-129">-Namespace</span></span>
<span data-ttu-id="e933d-130">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e933d-130">Namespace Name</span></span>

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

### <span data-ttu-id="e933d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e933d-131">-PassThru</span></span>
<span data-ttu-id="e933d-132">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e933d-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e933d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e933d-133">-ResourceGroupName</span></span>
<span data-ttu-id="e933d-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e933d-134">The name of the resource group</span></span>

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

### <span data-ttu-id="e933d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e933d-135">-ResourceId</span></span>
<span data-ttu-id="e933d-136">Идентификатор ресурса правила служебной шины</span><span class="sxs-lookup"><span data-stu-id="e933d-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="e933d-137">-Подписка</span><span class="sxs-lookup"><span data-stu-id="e933d-137">-Subscription</span></span>
<span data-ttu-id="e933d-138">Название подписки</span><span class="sxs-lookup"><span data-stu-id="e933d-138">Subscription Name</span></span>

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

### <span data-ttu-id="e933d-139">-Темы</span><span class="sxs-lookup"><span data-stu-id="e933d-139">-Topic</span></span>
<span data-ttu-id="e933d-140">Название раздела</span><span class="sxs-lookup"><span data-stu-id="e933d-140">Topic Name</span></span>

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

### <span data-ttu-id="e933d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e933d-141">-Confirm</span></span>
<span data-ttu-id="e933d-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e933d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e933d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e933d-143">-WhatIf</span></span>
<span data-ttu-id="e933d-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e933d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e933d-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e933d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e933d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e933d-146">CommonParameters</span></span>
<span data-ttu-id="e933d-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e933d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e933d-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e933d-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e933d-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e933d-149">INPUTS</span></span>

### <span data-ttu-id="e933d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e933d-150">System.String</span></span>

### <span data-ttu-id="e933d-151">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="e933d-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="e933d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e933d-152">OUTPUTS</span></span>

### <span data-ttu-id="e933d-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e933d-153">System.Boolean</span></span>

## <span data-ttu-id="e933d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="e933d-154">NOTES</span></span>

## <span data-ttu-id="e933d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e933d-155">RELATED LINKS</span></span>
