---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562179"
---
# <span data-ttu-id="17975-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="17975-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="17975-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17975-102">SYNOPSIS</span></span>
<span data-ttu-id="17975-103">Возвращает описание указанного правила авторизации для заданной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="17975-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17975-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17975-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17975-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17975-105">DESCRIPTION</span></span>
<span data-ttu-id="17975-106">Командлет **Get-AzureRmServiceBusQueueAuthorizationRule** получает описание указанного правила авторизации для заданной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="17975-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="17975-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17975-107">EXAMPLES</span></span>

### <span data-ttu-id="17975-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17975-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="17975-109">Возвращает указанное описание правила авторизации для данной очереди служебной шины.</span><span class="sxs-lookup"><span data-stu-id="17975-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="17975-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17975-110">PARAMETERS</span></span>

### <span data-ttu-id="17975-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17975-111">-ResourceGroup</span></span>
<span data-ttu-id="17975-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="17975-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="17975-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17975-113">-DefaultProfile</span></span>
<span data-ttu-id="17975-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17975-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17975-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17975-115">-Name</span></span>
<span data-ttu-id="17975-116">Имя AuthorizationRule EventHub.</span><span class="sxs-lookup"><span data-stu-id="17975-116">EventHub AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17975-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="17975-117">-Namespace</span></span>
<span data-ttu-id="17975-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="17975-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17975-119">-Очередь</span><span class="sxs-lookup"><span data-stu-id="17975-119">-Queue</span></span>
<span data-ttu-id="17975-120">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="17975-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17975-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17975-121">CommonParameters</span></span>
<span data-ttu-id="17975-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17975-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17975-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17975-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17975-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17975-124">INPUTS</span></span>

### <span data-ttu-id="17975-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="17975-125">-ResourceGroup</span></span>
 <span data-ttu-id="17975-126">System. String</span><span class="sxs-lookup"><span data-stu-id="17975-126">System.String</span></span>
 

### <span data-ttu-id="17975-127">-+ +</span><span class="sxs-lookup"><span data-stu-id="17975-127">-NamespaceName</span></span>
 <span data-ttu-id="17975-128">System. String</span><span class="sxs-lookup"><span data-stu-id="17975-128">System.String</span></span>
 

### <span data-ttu-id="17975-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="17975-129">-QueueName</span></span>
 <span data-ttu-id="17975-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17975-130">System.String</span></span>
 

### <span data-ttu-id="17975-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="17975-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="17975-132">System. String</span><span class="sxs-lookup"><span data-stu-id="17975-132">System.String</span></span>

## <span data-ttu-id="17975-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17975-133">OUTPUTS</span></span>

### <span data-ttu-id="17975-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="17975-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="17975-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onruless/SBAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules имя: SBAuthoRule1 расположение: Западная часть тегов US: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="17975-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="17975-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="17975-136">NOTES</span></span>

## <span data-ttu-id="17975-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17975-137">RELATED LINKS</span></span>

