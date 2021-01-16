---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0f765f8cf59453ee8b89317da2fa123785ee7f90
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400244"
---
# <span data-ttu-id="e5c0d-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="e5c0d-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="e5c0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c0d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c0d-103">Извлекает определение существующего правила в подписке на раздел.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-103">Retrieves the definition of an existing rule in a given Subscription of Topic.</span></span> 

## <span data-ttu-id="e5c0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5c0d-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5c0d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c0d-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c0d-106">С **его учетом** можно получить описание указанного правила в данной подписке.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="e5c0d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c0d-107">EXAMPLES</span></span>

### <span data-ttu-id="e5c0d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5c0d-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="e5c0d-109">Возвращает описание заданного правила для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="e5c0d-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5c0d-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="e5c0d-111">Возвращает список описаний правил для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="e5c0d-112">По умолчанию возвращается 100 правил, если возвращается более 100 правил, используйте параметр -MaxCount.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="e5c0d-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e5c0d-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="e5c0d-114">Возвращает список из первых 150 описаний правил для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="e5c0d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5c0d-115">PARAMETERS</span></span>

### <span data-ttu-id="e5c0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c0d-116">-DefaultProfile</span></span>
<span data-ttu-id="e5c0d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c0d-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e5c0d-118">-MaxCount</span></span>
<span data-ttu-id="e5c0d-119">Определите максимальное число возвращаемых правил.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="e5c0d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e5c0d-120">-Name</span></span>
<span data-ttu-id="e5c0d-121">Имя правила</span><span class="sxs-lookup"><span data-stu-id="e5c0d-121">Rule Name</span></span>

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

### <span data-ttu-id="e5c0d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5c0d-122">-Namespace</span></span>
<span data-ttu-id="e5c0d-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e5c0d-123">Namespace Name</span></span>

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

### <span data-ttu-id="e5c0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e5c0d-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e5c0d-125">The name of the resource group</span></span>

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

### <span data-ttu-id="e5c0d-126">-Подписка</span><span class="sxs-lookup"><span data-stu-id="e5c0d-126">-Subscription</span></span>
<span data-ttu-id="e5c0d-127">Название подписки</span><span class="sxs-lookup"><span data-stu-id="e5c0d-127">Subscription Name</span></span>

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

### <span data-ttu-id="e5c0d-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="e5c0d-128">-Topic</span></span>
<span data-ttu-id="e5c0d-129">Название темы</span><span class="sxs-lookup"><span data-stu-id="e5c0d-129">Topic Name</span></span>

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

### <span data-ttu-id="e5c0d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c0d-130">CommonParameters</span></span>
<span data-ttu-id="e5c0d-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c0d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c0d-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c0d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c0d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c0d-133">INPUTS</span></span>

### <span data-ttu-id="e5c0d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e5c0d-134">System.String</span></span>

## <span data-ttu-id="e5c0d-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c0d-135">OUTPUTS</span></span>

### <span data-ttu-id="e5c0d-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e5c0d-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="e5c0d-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5c0d-137">NOTES</span></span>

## <span data-ttu-id="e5c0d-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c0d-138">RELATED LINKS</span></span>
