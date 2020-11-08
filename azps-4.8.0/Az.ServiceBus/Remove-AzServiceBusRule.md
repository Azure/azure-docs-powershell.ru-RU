---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077610"
---
# <span data-ttu-id="9705b-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="9705b-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="9705b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9705b-102">SYNOPSIS</span></span>
<span data-ttu-id="9705b-103">Удаляет указанное правило данной подписки.</span><span class="sxs-lookup"><span data-stu-id="9705b-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="9705b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9705b-104">SYNTAX</span></span>

### <span data-ttu-id="9705b-105">RulePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9705b-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9705b-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9705b-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9705b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9705b-107">DESCRIPTION</span></span>
<span data-ttu-id="9705b-108">Командлет **Remove-AzServiceBusRule** удаляет правило подписки на данную тему.</span><span class="sxs-lookup"><span data-stu-id="9705b-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="9705b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9705b-109">EXAMPLES</span></span>

### <span data-ttu-id="9705b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9705b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="9705b-111">Удаляет правило `SBRule` подписки `SBSubscription` для указанной темы `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="9705b-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="9705b-112">Пример 2: InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="9705b-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="9705b-113">Удаляет правило, указанное в параметре $inputobject для параметра-InputObject</span><span class="sxs-lookup"><span data-stu-id="9705b-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="9705b-114">Пример 3: InputObject — использование трубопроводов:</span><span class="sxs-lookup"><span data-stu-id="9705b-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="9705b-115">Пример 4: ResourceId — использование переменной</span><span class="sxs-lookup"><span data-stu-id="9705b-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="9705b-116">Пример 5: ResourceId — использование строкового значения</span><span class="sxs-lookup"><span data-stu-id="9705b-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="9705b-117">Удаляет правило, указанное с помощью идентификатора ARM, в $resourceid/String для-ResourceId (параметр)</span><span class="sxs-lookup"><span data-stu-id="9705b-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="9705b-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9705b-118">PARAMETERS</span></span>

### <span data-ttu-id="9705b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9705b-119">-AsJob</span></span>
<span data-ttu-id="9705b-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9705b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9705b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9705b-121">-DefaultProfile</span></span>
<span data-ttu-id="9705b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9705b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9705b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9705b-123">-Force</span></span>
<span data-ttu-id="9705b-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9705b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9705b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9705b-125">-InputObject</span></span>
<span data-ttu-id="9705b-126">Объект правила служебной шины</span><span class="sxs-lookup"><span data-stu-id="9705b-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="9705b-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9705b-127">-Name</span></span>
<span data-ttu-id="9705b-128">Имя правила</span><span class="sxs-lookup"><span data-stu-id="9705b-128">Rule Name</span></span>

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

### <span data-ttu-id="9705b-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9705b-129">-Namespace</span></span>
<span data-ttu-id="9705b-130">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="9705b-130">Namespace Name</span></span>

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

### <span data-ttu-id="9705b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9705b-131">-PassThru</span></span>
<span data-ttu-id="9705b-132">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9705b-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9705b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9705b-133">-ResourceGroupName</span></span>
<span data-ttu-id="9705b-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9705b-134">The name of the resource group</span></span>

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

### <span data-ttu-id="9705b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9705b-135">-ResourceId</span></span>
<span data-ttu-id="9705b-136">Идентификатор ресурса правила служебной шины</span><span class="sxs-lookup"><span data-stu-id="9705b-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="9705b-137">-Подписка</span><span class="sxs-lookup"><span data-stu-id="9705b-137">-Subscription</span></span>
<span data-ttu-id="9705b-138">Название подписки</span><span class="sxs-lookup"><span data-stu-id="9705b-138">Subscription Name</span></span>

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

### <span data-ttu-id="9705b-139">-Темы</span><span class="sxs-lookup"><span data-stu-id="9705b-139">-Topic</span></span>
<span data-ttu-id="9705b-140">Название раздела</span><span class="sxs-lookup"><span data-stu-id="9705b-140">Topic Name</span></span>

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

### <span data-ttu-id="9705b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9705b-141">-Confirm</span></span>
<span data-ttu-id="9705b-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9705b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9705b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9705b-143">-WhatIf</span></span>
<span data-ttu-id="9705b-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9705b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9705b-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9705b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9705b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9705b-146">CommonParameters</span></span>
<span data-ttu-id="9705b-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9705b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9705b-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9705b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9705b-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9705b-149">INPUTS</span></span>

### <span data-ttu-id="9705b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9705b-150">System.String</span></span>

### <span data-ttu-id="9705b-151">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="9705b-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="9705b-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9705b-152">OUTPUTS</span></span>

### <span data-ttu-id="9705b-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9705b-153">System.Boolean</span></span>

## <span data-ttu-id="9705b-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="9705b-154">NOTES</span></span>

## <span data-ttu-id="9705b-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9705b-155">RELATED LINKS</span></span>
