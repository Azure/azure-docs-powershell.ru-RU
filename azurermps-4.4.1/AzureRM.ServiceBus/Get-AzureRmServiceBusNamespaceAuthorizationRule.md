---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565134"
---
# <span data-ttu-id="d15ca-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d15ca-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="d15ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d15ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d15ca-103">Возвращает описание указанного правила авторизации для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d15ca-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d15ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d15ca-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d15ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d15ca-105">DESCRIPTION</span></span>
<span data-ttu-id="d15ca-106">Командлет **Get-AzureRmServiceBusNamespaceAuthorizationRule** получает описание указанного правила авторизации в заданном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d15ca-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="d15ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d15ca-107">EXAMPLES</span></span>

### <span data-ttu-id="d15ca-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d15ca-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="d15ca-109">Возвращает указанное описание правила авторизации для указанного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d15ca-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="d15ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d15ca-110">PARAMETERS</span></span>

### <span data-ttu-id="d15ca-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d15ca-111">-ResourceGroup</span></span>
<span data-ttu-id="d15ca-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d15ca-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="d15ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15ca-113">-DefaultProfile</span></span>
<span data-ttu-id="d15ca-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d15ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d15ca-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d15ca-115">-Name</span></span>
<span data-ttu-id="d15ca-116">Имя AuthorizationRule пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="d15ca-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="d15ca-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d15ca-117">-Namespace</span></span>
<span data-ttu-id="d15ca-118">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="d15ca-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="d15ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15ca-119">CommonParameters</span></span>
<span data-ttu-id="d15ca-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d15ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15ca-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15ca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15ca-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d15ca-122">INPUTS</span></span>

### <span data-ttu-id="d15ca-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d15ca-123">-ResourceGroup</span></span>
 <span data-ttu-id="d15ca-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d15ca-124">System.String</span></span>
 

### <span data-ttu-id="d15ca-125">-+ +</span><span class="sxs-lookup"><span data-stu-id="d15ca-125">-NamespaceName</span></span>
 <span data-ttu-id="d15ca-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d15ca-126">System.String</span></span>
 

### <span data-ttu-id="d15ca-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="d15ca-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="d15ca-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d15ca-128">System.String</span></span>

## <span data-ttu-id="d15ca-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d15ca-129">OUTPUTS</span></span>

### <span data-ttu-id="d15ca-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="d15ca-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d15ca-131">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 тип: Microsoft. ServiceBus/AuthorizationRules: AuthoRule1 расположение: Теги: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="d15ca-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="d15ca-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d15ca-132">NOTES</span></span>

## <span data-ttu-id="d15ca-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d15ca-133">RELATED LINKS</span></span>

