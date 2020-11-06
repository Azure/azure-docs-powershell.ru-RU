---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0dc0e2ebf22d995577abd37e2eef2b16b0ea4001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566908"
---
# <span data-ttu-id="512ea-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="512ea-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="512ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="512ea-102">SYNOPSIS</span></span>
<span data-ttu-id="512ea-103">Повторно создает первичные или дополнительные строки подключения для пространства имен служебной шины или очереди или темы.</span><span class="sxs-lookup"><span data-stu-id="512ea-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="512ea-104">SYNTAX</span></span>

### <span data-ttu-id="512ea-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="512ea-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="512ea-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="512ea-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="512ea-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="512ea-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="512ea-108">DESCRIPTION</span></span>
<span data-ttu-id="512ea-109">Командлет **New-AzureRmServiceBusKey** создает новые первичные или дополнительные строки подключения для указанного пространства имен, очереди или темы и правила авторизации.</span><span class="sxs-lookup"><span data-stu-id="512ea-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="512ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="512ea-110">EXAMPLES</span></span>

### <span data-ttu-id="512ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="512ea-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="512ea-112">Повторно создает первичные или дополнительные строки подключения для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="512ea-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="512ea-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="512ea-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="512ea-114">Повторно создает первичные или дополнительные строки подключения для очереди.</span><span class="sxs-lookup"><span data-stu-id="512ea-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="512ea-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="512ea-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="512ea-116">Повторно создает первичные или дополнительные строки подключения для темы.</span><span class="sxs-lookup"><span data-stu-id="512ea-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="512ea-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="512ea-117">PARAMETERS</span></span>

### <span data-ttu-id="512ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512ea-118">-DefaultProfile</span></span>
<span data-ttu-id="512ea-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="512ea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="512ea-120">-Name</span></span>
<span data-ttu-id="512ea-121">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="512ea-121">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="512ea-122">-Namespace</span></span>
<span data-ttu-id="512ea-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="512ea-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="512ea-124">-Queue</span></span>
<span data-ttu-id="512ea-125">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="512ea-125">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="512ea-126">-RegenerateKey</span></span>
<span data-ttu-id="512ea-127">Повторное создание ключей-"PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="512ea-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="512ea-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="512ea-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-130">-Темы</span><span class="sxs-lookup"><span data-stu-id="512ea-130">-Topic</span></span>
<span data-ttu-id="512ea-131">Название раздела</span><span class="sxs-lookup"><span data-stu-id="512ea-131">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="512ea-132">-Confirm</span></span>
<span data-ttu-id="512ea-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="512ea-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512ea-134">-WhatIf</span></span>
<span data-ttu-id="512ea-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="512ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512ea-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="512ea-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512ea-137">CommonParameters</span></span>
<span data-ttu-id="512ea-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="512ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="512ea-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512ea-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512ea-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="512ea-140">INPUTS</span></span>

### <span data-ttu-id="512ea-141">System. String</span><span class="sxs-lookup"><span data-stu-id="512ea-141">System.String</span></span>


## <span data-ttu-id="512ea-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="512ea-142">OUTPUTS</span></span>

### <span data-ttu-id="512ea-143">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="512ea-143">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="512ea-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="512ea-144">NOTES</span></span>

## <span data-ttu-id="512ea-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="512ea-145">RELATED LINKS</span></span>
