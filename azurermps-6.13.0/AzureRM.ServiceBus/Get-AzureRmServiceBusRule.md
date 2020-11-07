---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732899"
---
# <span data-ttu-id="0d06c-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="0d06c-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="0d06c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d06c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d06c-103">Создает новое правило для конкретной подписки на тему.</span><span class="sxs-lookup"><span data-stu-id="0d06c-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d06c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d06c-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d06c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d06c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d06c-106">Командлет **Get-AzureRmServiceBusRule** получает описание указанного правила в заданной подписке на тему.</span><span class="sxs-lookup"><span data-stu-id="0d06c-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="0d06c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d06c-107">EXAMPLES</span></span>

### <span data-ttu-id="0d06c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d06c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="0d06c-109">Возвращает указанное описание правила для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="0d06c-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="0d06c-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0d06c-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="0d06c-111">Возвращает список описаний правил для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="0d06c-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="0d06c-112">По умолчанию возвращается правило 100, если возвращено больше чем 100 правило, используйте параметр-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="0d06c-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="0d06c-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0d06c-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="0d06c-114">Возвращает список описаний первых правил 150 для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="0d06c-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="0d06c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d06c-115">PARAMETERS</span></span>

### <span data-ttu-id="0d06c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d06c-116">-DefaultProfile</span></span>
<span data-ttu-id="0d06c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d06c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d06c-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0d06c-118">-MaxCount</span></span>
<span data-ttu-id="0d06c-119">Определение максимального числа возвращаемых правил.</span><span class="sxs-lookup"><span data-stu-id="0d06c-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d06c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d06c-120">-Name</span></span>
<span data-ttu-id="0d06c-121">Имя правила</span><span class="sxs-lookup"><span data-stu-id="0d06c-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d06c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0d06c-122">-Namespace</span></span>
<span data-ttu-id="0d06c-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="0d06c-123">Namespace Name</span></span>

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

### <span data-ttu-id="0d06c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d06c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d06c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d06c-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d06c-126">-Подписка</span><span class="sxs-lookup"><span data-stu-id="0d06c-126">-Subscription</span></span>
<span data-ttu-id="0d06c-127">Название подписки</span><span class="sxs-lookup"><span data-stu-id="0d06c-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d06c-128">-Темы</span><span class="sxs-lookup"><span data-stu-id="0d06c-128">-Topic</span></span>
<span data-ttu-id="0d06c-129">Название раздела</span><span class="sxs-lookup"><span data-stu-id="0d06c-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d06c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d06c-130">CommonParameters</span></span>
<span data-ttu-id="0d06c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d06c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d06c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d06c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d06c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d06c-133">INPUTS</span></span>

### <span data-ttu-id="0d06c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0d06c-134">System.String</span></span>

## <span data-ttu-id="0d06c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d06c-135">OUTPUTS</span></span>

### <span data-ttu-id="0d06c-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0d06c-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="0d06c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d06c-137">NOTES</span></span>

## <span data-ttu-id="0d06c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d06c-138">RELATED LINKS</span></span>
