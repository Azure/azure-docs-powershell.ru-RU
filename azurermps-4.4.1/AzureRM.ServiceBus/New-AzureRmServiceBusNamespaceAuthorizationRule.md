---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734228"
---
# <span data-ttu-id="082c1-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="082c1-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="082c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="082c1-102">SYNOPSIS</span></span>
<span data-ttu-id="082c1-103">Создает новое правило авторизации для указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="082c1-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="082c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="082c1-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="082c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="082c1-105">DESCRIPTION</span></span>
<span data-ttu-id="082c1-106">Командлет **New-AzureRmServiceBusNamespaceAuthorizationRule** создает новое правило авторизации для указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="082c1-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="082c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="082c1-107">EXAMPLES</span></span>

### <span data-ttu-id="082c1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="082c1-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="082c1-109">Создание `AuthoRule1` с правами на **прослушивание** и **отправку** для пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="082c1-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="082c1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="082c1-110">PARAMETERS</span></span>

### <span data-ttu-id="082c1-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="082c1-111">-ResourceGroup</span></span>
<span data-ttu-id="082c1-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="082c1-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="082c1-113">-Права</span><span class="sxs-lookup"><span data-stu-id="082c1-113">-Rights</span></span>
<span data-ttu-id="082c1-114">Права доступа; Например, @ ("прослушать", "Отправить", "Управление")</span><span class="sxs-lookup"><span data-stu-id="082c1-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="082c1-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="082c1-115">-Confirm</span></span>
<span data-ttu-id="082c1-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="082c1-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082c1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082c1-117">-WhatIf</span></span>
<span data-ttu-id="082c1-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="082c1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="082c1-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="082c1-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="082c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082c1-120">-DefaultProfile</span></span>
<span data-ttu-id="082c1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="082c1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="082c1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="082c1-122">-Name</span></span>
<span data-ttu-id="082c1-123">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="082c1-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="082c1-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="082c1-124">-Namespace</span></span>
<span data-ttu-id="082c1-125">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="082c1-125">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="082c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082c1-126">CommonParameters</span></span>
<span data-ttu-id="082c1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="082c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082c1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082c1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082c1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="082c1-129">INPUTS</span></span>

### <span data-ttu-id="082c1-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="082c1-130">-ResourceGroup</span></span>
 <span data-ttu-id="082c1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="082c1-131">System.String</span></span>
 

### <span data-ttu-id="082c1-132">-+ +</span><span class="sxs-lookup"><span data-stu-id="082c1-132">-NamespaceName</span></span>
 <span data-ttu-id="082c1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="082c1-133">System.String</span></span>
 

### <span data-ttu-id="082c1-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="082c1-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="082c1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="082c1-135">System.String</span></span>
 

### <span data-ttu-id="082c1-136">-Права</span><span class="sxs-lookup"><span data-stu-id="082c1-136">-Rights</span></span>
 <span data-ttu-id="082c1-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="082c1-137">System.String []</span></span>

## <span data-ttu-id="082c1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="082c1-138">OUTPUTS</span></span>

### <span data-ttu-id="082c1-139">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="082c1-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="082c1-140">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 тип: Microsoft. ServiceBus/AuthorizationRules: AuthoRule1 расположение: Теги: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="082c1-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="082c1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="082c1-141">NOTES</span></span>

## <span data-ttu-id="082c1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="082c1-142">RELATED LINKS</span></span>

