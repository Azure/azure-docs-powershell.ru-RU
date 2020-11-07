---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733219"
---
# <span data-ttu-id="6dd06-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="6dd06-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="6dd06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dd06-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd06-103">Создает новое правило для конкретной подписки на тему.</span><span class="sxs-lookup"><span data-stu-id="6dd06-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dd06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dd06-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dd06-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd06-106">Командлет **New-AzureRmServiceBusRule** создает новое правило для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="6dd06-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="6dd06-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dd06-107">EXAMPLES</span></span>

### <span data-ttu-id="6dd06-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6dd06-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="6dd06-109">Командлет New-AzureRmServiceBusRule создает новое правило для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="6dd06-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="6dd06-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dd06-110">PARAMETERS</span></span>

### <span data-ttu-id="6dd06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd06-111">-DefaultProfile</span></span>
<span data-ttu-id="6dd06-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dd06-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6dd06-113">-Name</span></span>
<span data-ttu-id="6dd06-114">Имя правила</span><span class="sxs-lookup"><span data-stu-id="6dd06-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd06-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6dd06-115">-Namespace</span></span>
<span data-ttu-id="6dd06-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6dd06-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6dd06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dd06-117">-ResourceGroupName</span></span>
<span data-ttu-id="6dd06-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6dd06-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd06-119">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="6dd06-119">-SqlExpression</span></span>
<span data-ttu-id="6dd06-120">Выражение SQL фильтрацию</span><span class="sxs-lookup"><span data-stu-id="6dd06-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd06-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="6dd06-121">-Subscription</span></span>
<span data-ttu-id="6dd06-122">Название подписки</span><span class="sxs-lookup"><span data-stu-id="6dd06-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd06-123">-Темы</span><span class="sxs-lookup"><span data-stu-id="6dd06-123">-Topic</span></span>
<span data-ttu-id="6dd06-124">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="6dd06-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd06-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dd06-125">-Confirm</span></span>
<span data-ttu-id="6dd06-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6dd06-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd06-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd06-127">-WhatIf</span></span>
<span data-ttu-id="6dd06-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6dd06-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd06-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6dd06-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd06-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd06-130">CommonParameters</span></span>
<span data-ttu-id="6dd06-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dd06-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd06-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd06-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd06-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dd06-133">INPUTS</span></span>

### <span data-ttu-id="6dd06-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6dd06-134">System.String</span></span>

## <span data-ttu-id="6dd06-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dd06-135">OUTPUTS</span></span>

### <span data-ttu-id="6dd06-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="6dd06-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="6dd06-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dd06-137">NOTES</span></span>

## <span data-ttu-id="6dd06-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dd06-138">RELATED LINKS</span></span>

