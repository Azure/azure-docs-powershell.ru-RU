---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: b4e008dcb80cf1b67e7987fe89d86c89f247476c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073723"
---
# <span data-ttu-id="736b5-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="736b5-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="736b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="736b5-102">SYNOPSIS</span></span>
<span data-ttu-id="736b5-103">Повторно создает первичные или дополнительные строки подключения для пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="736b5-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="736b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="736b5-104">SYNTAX</span></span>

### <span data-ttu-id="736b5-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="736b5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="736b5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="736b5-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="736b5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="736b5-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="736b5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="736b5-108">DESCRIPTION</span></span>
<span data-ttu-id="736b5-109">Командлет **New-AzServiceBusKey** создает новые первичные или дополнительные строки подключения для указанного пространства имен, очереди или темы и правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="736b5-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="736b5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="736b5-110">EXAMPLES</span></span>

### <span data-ttu-id="736b5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="736b5-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="736b5-112">Повторно создает первичные или дополнительные строки подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="736b5-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="736b5-113">Пример 1,1</span><span class="sxs-lookup"><span data-stu-id="736b5-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="736b5-114">Повторно создает первичные или дополнительные строки подключения с указанным значением ключа для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="736b5-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="736b5-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="736b5-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="736b5-116">Повторно создает первичные или дополнительные строки подключения для очереди.</span><span class="sxs-lookup"><span data-stu-id="736b5-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="736b5-117">Пример 2,2</span><span class="sxs-lookup"><span data-stu-id="736b5-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="736b5-118">Повторно создает первичные или дополнительные строки подключения с указанным значением ключа для очереди.</span><span class="sxs-lookup"><span data-stu-id="736b5-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="736b5-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="736b5-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="736b5-120">Повторно создает первичные или дополнительные строки подключения для темы.</span><span class="sxs-lookup"><span data-stu-id="736b5-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="736b5-121">Пример 3,1</span><span class="sxs-lookup"><span data-stu-id="736b5-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="736b5-122">Повторно создает первичные или дополнительные строки подключения с указанным значением ключа для темы.</span><span class="sxs-lookup"><span data-stu-id="736b5-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="736b5-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="736b5-123">PARAMETERS</span></span>

### <span data-ttu-id="736b5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736b5-124">-DefaultProfile</span></span>
<span data-ttu-id="736b5-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="736b5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="736b5-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="736b5-126">-KeyValue</span></span>
<span data-ttu-id="736b5-127">256-разрядный ключ в формате Base64 для подписывания и проверки маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="736b5-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="736b5-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="736b5-128">-Name</span></span>
<span data-ttu-id="736b5-129">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="736b5-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="736b5-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="736b5-130">-Namespace</span></span>
<span data-ttu-id="736b5-131">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="736b5-131">Namespace Name</span></span>

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

### <span data-ttu-id="736b5-132">-Очередь</span><span class="sxs-lookup"><span data-stu-id="736b5-132">-Queue</span></span>
<span data-ttu-id="736b5-133">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="736b5-133">Queue Name</span></span>

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

### <span data-ttu-id="736b5-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="736b5-134">-RegenerateKey</span></span>
<span data-ttu-id="736b5-135">Повторное создание ключей-"PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="736b5-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="736b5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="736b5-136">-ResourceGroupName</span></span>
<span data-ttu-id="736b5-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="736b5-137">Resource Group Name</span></span>

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

### <span data-ttu-id="736b5-138">-Темы</span><span class="sxs-lookup"><span data-stu-id="736b5-138">-Topic</span></span>
<span data-ttu-id="736b5-139">Название раздела</span><span class="sxs-lookup"><span data-stu-id="736b5-139">Topic Name</span></span>

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

### <span data-ttu-id="736b5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="736b5-140">-Confirm</span></span>
<span data-ttu-id="736b5-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="736b5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="736b5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="736b5-142">-WhatIf</span></span>
<span data-ttu-id="736b5-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="736b5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="736b5-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="736b5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="736b5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736b5-145">CommonParameters</span></span>
<span data-ttu-id="736b5-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="736b5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736b5-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736b5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736b5-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="736b5-148">INPUTS</span></span>

### <span data-ttu-id="736b5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="736b5-149">System.String</span></span>

## <span data-ttu-id="736b5-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="736b5-150">OUTPUTS</span></span>

### <span data-ttu-id="736b5-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="736b5-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="736b5-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="736b5-152">NOTES</span></span>

## <span data-ttu-id="736b5-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="736b5-153">RELATED LINKS</span></span>
