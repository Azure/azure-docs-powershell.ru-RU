---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: f4899d55919f8b3c08b36babc448f1594f4ac4c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073735"
---
# <span data-ttu-id="bdb45-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="bdb45-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="bdb45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdb45-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb45-103">Создает новое правило для конкретной подписки на тему.</span><span class="sxs-lookup"><span data-stu-id="bdb45-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="bdb45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdb45-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdb45-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb45-105">DESCRIPTION</span></span>
<span data-ttu-id="bdb45-106">Командлет **Get-AzServiceBusRule** получает описание указанного правила в заданной подписке на тему.</span><span class="sxs-lookup"><span data-stu-id="bdb45-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="bdb45-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdb45-107">EXAMPLES</span></span>

### <span data-ttu-id="bdb45-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bdb45-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="bdb45-109">Возвращает указанное описание правила для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="bdb45-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="bdb45-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bdb45-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="bdb45-111">Возвращает список описаний правил для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="bdb45-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="bdb45-112">По умолчанию возвращается правило 100, если возвращено больше чем 100 правило, используйте параметр-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="bdb45-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="bdb45-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bdb45-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="bdb45-114">Возвращает список описаний первых правил 150 для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="bdb45-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="bdb45-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdb45-115">PARAMETERS</span></span>

### <span data-ttu-id="bdb45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb45-116">-DefaultProfile</span></span>
<span data-ttu-id="bdb45-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb45-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bdb45-118">-MaxCount</span></span>
<span data-ttu-id="bdb45-119">Определение максимального числа возвращаемых правил.</span><span class="sxs-lookup"><span data-stu-id="bdb45-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="bdb45-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bdb45-120">-Name</span></span>
<span data-ttu-id="bdb45-121">Имя правила</span><span class="sxs-lookup"><span data-stu-id="bdb45-121">Rule Name</span></span>

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

### <span data-ttu-id="bdb45-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bdb45-122">-Namespace</span></span>
<span data-ttu-id="bdb45-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="bdb45-123">Namespace Name</span></span>

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

### <span data-ttu-id="bdb45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb45-124">-ResourceGroupName</span></span>
<span data-ttu-id="bdb45-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bdb45-125">The name of the resource group</span></span>

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

### <span data-ttu-id="bdb45-126">-Подписка</span><span class="sxs-lookup"><span data-stu-id="bdb45-126">-Subscription</span></span>
<span data-ttu-id="bdb45-127">Название подписки</span><span class="sxs-lookup"><span data-stu-id="bdb45-127">Subscription Name</span></span>

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

### <span data-ttu-id="bdb45-128">-Темы</span><span class="sxs-lookup"><span data-stu-id="bdb45-128">-Topic</span></span>
<span data-ttu-id="bdb45-129">Название раздела</span><span class="sxs-lookup"><span data-stu-id="bdb45-129">Topic Name</span></span>

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

### <span data-ttu-id="bdb45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb45-130">CommonParameters</span></span>
<span data-ttu-id="bdb45-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdb45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb45-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb45-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb45-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdb45-133">INPUTS</span></span>

### <span data-ttu-id="bdb45-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bdb45-134">System.String</span></span>

## <span data-ttu-id="bdb45-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdb45-135">OUTPUTS</span></span>

### <span data-ttu-id="bdb45-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="bdb45-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="bdb45-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdb45-137">NOTES</span></span>

## <span data-ttu-id="bdb45-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdb45-138">RELATED LINKS</span></span>
