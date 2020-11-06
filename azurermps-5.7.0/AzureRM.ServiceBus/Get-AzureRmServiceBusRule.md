---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567920"
---
# <span data-ttu-id="a6803-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="a6803-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="a6803-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6803-102">SYNOPSIS</span></span>
<span data-ttu-id="a6803-103">Возвращает описание указанного правила для данной подписки на тему.</span><span class="sxs-lookup"><span data-stu-id="a6803-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6803-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6803-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6803-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6803-105">DESCRIPTION</span></span>
<span data-ttu-id="a6803-106">Командлет **Get-AzureRmServiceBusRule** получает описание указанного правила в заданной подписке на тему.</span><span class="sxs-lookup"><span data-stu-id="a6803-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="a6803-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6803-107">EXAMPLES</span></span>

### <span data-ttu-id="a6803-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6803-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="a6803-109">Возвращает указанное описание правила для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="a6803-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="a6803-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6803-110">PARAMETERS</span></span>

### <span data-ttu-id="a6803-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6803-111">-DefaultProfile</span></span>
<span data-ttu-id="a6803-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6803-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6803-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6803-113">-Name</span></span>
<span data-ttu-id="a6803-114">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="a6803-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6803-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a6803-115">-Namespace</span></span>
<span data-ttu-id="a6803-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a6803-116">Namespace Name.</span></span>

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

### <span data-ttu-id="a6803-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6803-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6803-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6803-118">The name of the resource group</span></span>

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

### <span data-ttu-id="a6803-119">-Подписка</span><span class="sxs-lookup"><span data-stu-id="a6803-119">-Subscription</span></span>
<span data-ttu-id="a6803-120">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="a6803-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6803-121">-Темы</span><span class="sxs-lookup"><span data-stu-id="a6803-121">-Topic</span></span>
<span data-ttu-id="a6803-122">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="a6803-122">Topic Name.</span></span>

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

### <span data-ttu-id="a6803-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6803-123">CommonParameters</span></span>
<span data-ttu-id="a6803-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6803-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6803-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6803-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6803-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6803-126">INPUTS</span></span>

### <span data-ttu-id="a6803-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a6803-127">System.String</span></span>

## <span data-ttu-id="a6803-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6803-128">OUTPUTS</span></span>

### <span data-ttu-id="a6803-129">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a6803-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="a6803-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6803-130">NOTES</span></span>

## <span data-ttu-id="a6803-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6803-131">RELATED LINKS</span></span>

