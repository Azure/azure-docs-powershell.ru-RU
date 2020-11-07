---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: 46a3551e309504d9938359a0fed4d37860fcb524
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729185"
---
# <span data-ttu-id="85e34-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="85e34-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="85e34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85e34-102">SYNOPSIS</span></span>
<span data-ttu-id="85e34-103">Повторно создает первичные или дополнительные строки подключения для пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="85e34-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="85e34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85e34-104">SYNTAX</span></span>

### <span data-ttu-id="85e34-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85e34-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85e34-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="85e34-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85e34-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="85e34-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85e34-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85e34-108">DESCRIPTION</span></span>
<span data-ttu-id="85e34-109">Командлет **New-AzServiceBusKey** создает новые первичные или дополнительные строки подключения для указанного пространства имен, очереди или темы и правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="85e34-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="85e34-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85e34-110">EXAMPLES</span></span>

### <span data-ttu-id="85e34-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85e34-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="85e34-112">Повторно создает первичные или дополнительные строки подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="85e34-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="85e34-113">Пример 1,1</span><span class="sxs-lookup"><span data-stu-id="85e34-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="85e34-114">Повторно создает первичные или дополнительные строки подключения с указанным значением ключа для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="85e34-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="85e34-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="85e34-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="85e34-116">Повторно создает первичные или дополнительные строки подключения для очереди.</span><span class="sxs-lookup"><span data-stu-id="85e34-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="85e34-117">Пример 2,2</span><span class="sxs-lookup"><span data-stu-id="85e34-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="85e34-118">Повторно создает первичные или дополнительные строки подключения с указанным значением ключа для очереди.</span><span class="sxs-lookup"><span data-stu-id="85e34-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="85e34-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="85e34-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="85e34-120">Повторно создает первичные или дополнительные строки подключения для темы.</span><span class="sxs-lookup"><span data-stu-id="85e34-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="85e34-121">Пример 3,1</span><span class="sxs-lookup"><span data-stu-id="85e34-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="85e34-122">Повторно создает первичные или дополнительные строки подключения с указанным значением ключа для темы.</span><span class="sxs-lookup"><span data-stu-id="85e34-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="85e34-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85e34-123">PARAMETERS</span></span>

### <span data-ttu-id="85e34-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e34-124">-DefaultProfile</span></span>
<span data-ttu-id="85e34-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85e34-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85e34-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="85e34-126">-KeyValue</span></span>
<span data-ttu-id="85e34-127">256-разрядный ключ в формате Base64 для подписывания и проверки маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="85e34-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85e34-128">-Name</span></span>
<span data-ttu-id="85e34-129">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="85e34-129">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="85e34-130">-Namespace</span></span>
<span data-ttu-id="85e34-131">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="85e34-131">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-132">-Очередь</span><span class="sxs-lookup"><span data-stu-id="85e34-132">-Queue</span></span>
<span data-ttu-id="85e34-133">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="85e34-133">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="85e34-134">-RegenerateKey</span></span>
<span data-ttu-id="85e34-135">Повторное создание ключей-"PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="85e34-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e34-136">-ResourceGroupName</span></span>
<span data-ttu-id="85e34-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="85e34-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-138">-Темы</span><span class="sxs-lookup"><span data-stu-id="85e34-138">-Topic</span></span>
<span data-ttu-id="85e34-139">Название раздела</span><span class="sxs-lookup"><span data-stu-id="85e34-139">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e34-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85e34-140">-Confirm</span></span>
<span data-ttu-id="85e34-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85e34-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e34-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85e34-142">-WhatIf</span></span>
<span data-ttu-id="85e34-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85e34-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85e34-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85e34-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e34-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e34-145">CommonParameters</span></span>
<span data-ttu-id="85e34-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85e34-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e34-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e34-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e34-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85e34-148">INPUTS</span></span>

### <span data-ttu-id="85e34-149">System. String</span><span class="sxs-lookup"><span data-stu-id="85e34-149">System.String</span></span>

## <span data-ttu-id="85e34-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85e34-150">OUTPUTS</span></span>

### <span data-ttu-id="85e34-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="85e34-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="85e34-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="85e34-152">NOTES</span></span>

## <span data-ttu-id="85e34-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85e34-153">RELATED LINKS</span></span>
