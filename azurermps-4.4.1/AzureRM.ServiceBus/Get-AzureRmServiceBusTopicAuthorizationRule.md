---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568306"
---
# <span data-ttu-id="47838-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="47838-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="47838-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47838-102">SYNOPSIS</span></span>
<span data-ttu-id="47838-103">Возвращает описание указанного описания правила авторизации для данной темы.</span><span class="sxs-lookup"><span data-stu-id="47838-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47838-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47838-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47838-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47838-105">DESCRIPTION</span></span>
<span data-ttu-id="47838-106">Командлет **Get-AzureRmServiceBusTopicAuthorizationRule** получает описание указанного правила авторизации для заданной темы служебной шины.</span><span class="sxs-lookup"><span data-stu-id="47838-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="47838-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47838-107">EXAMPLES</span></span>

### <span data-ttu-id="47838-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47838-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="47838-109">Возвращает описание указанного правила авторизации для данной темы.</span><span class="sxs-lookup"><span data-stu-id="47838-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="47838-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47838-110">PARAMETERS</span></span>

### <span data-ttu-id="47838-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47838-111">-ResourceGroup</span></span>
<span data-ttu-id="47838-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47838-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="47838-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47838-113">-DefaultProfile</span></span>
<span data-ttu-id="47838-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47838-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47838-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47838-115">-Name</span></span>
<span data-ttu-id="47838-116">Название темы AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="47838-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="47838-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="47838-117">-Namespace</span></span>
<span data-ttu-id="47838-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="47838-118">Namespace Name.</span></span>

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

### <span data-ttu-id="47838-119">-Темы</span><span class="sxs-lookup"><span data-stu-id="47838-119">-Topic</span></span>
<span data-ttu-id="47838-120">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="47838-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47838-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47838-121">CommonParameters</span></span>
<span data-ttu-id="47838-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47838-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47838-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47838-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47838-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47838-124">INPUTS</span></span>

### <span data-ttu-id="47838-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47838-125">-ResourceGroup</span></span>
 <span data-ttu-id="47838-126">System. String</span><span class="sxs-lookup"><span data-stu-id="47838-126">System.String</span></span>
 

### <span data-ttu-id="47838-127">-+ +</span><span class="sxs-lookup"><span data-stu-id="47838-127">-NamespaceName</span></span>
 <span data-ttu-id="47838-128">System. String</span><span class="sxs-lookup"><span data-stu-id="47838-128">System.String</span></span>
 

### <span data-ttu-id="47838-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="47838-129">-TopicName</span></span>
 <span data-ttu-id="47838-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47838-130">System.String</span></span>
 

### <span data-ttu-id="47838-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="47838-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="47838-132">System. String</span><span class="sxs-lookup"><span data-stu-id="47838-132">System.String</span></span>

## <span data-ttu-id="47838-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47838-133">OUTPUTS</span></span>

### <span data-ttu-id="47838-134">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="47838-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="47838-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onruless/SBTopicAuthoRule1 Type: Microsoft. ServiceBus/AuthorizationRules имя: SBTopicAuthoRule1 расположение: Западная часть тегов US: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="47838-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="47838-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="47838-136">NOTES</span></span>

## <span data-ttu-id="47838-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47838-137">RELATED LINKS</span></span>

