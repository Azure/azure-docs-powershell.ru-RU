---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734516"
---
# <span data-ttu-id="4db99-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4db99-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="4db99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4db99-102">SYNOPSIS</span></span>
<span data-ttu-id="4db99-103">Обновляет указанное описание правила авторизации для заданного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4db99-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4db99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4db99-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4db99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4db99-105">DESCRIPTION</span></span>
<span data-ttu-id="4db99-106">Командлет **Set-AzureRmServiceBusNamespaceAuthorizationRule** обновляет описание указанного правила авторизации в заданном пространстве имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="4db99-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="4db99-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4db99-107">EXAMPLES</span></span>

### <span data-ttu-id="4db99-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4db99-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="4db99-109">Удаляет **Управление** из прав доступа правила авторизации `AuthoRule1` в пространстве имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="4db99-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="4db99-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4db99-110">PARAMETERS</span></span>

### <span data-ttu-id="4db99-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4db99-111">-ResourceGroup</span></span>
<span data-ttu-id="4db99-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4db99-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="4db99-113">-Права</span><span class="sxs-lookup"><span data-stu-id="4db99-113">-Rights</span></span>
<span data-ttu-id="4db99-114">Администратора Например, @ ("прослушать", "Отправить", "Управление").</span><span class="sxs-lookup"><span data-stu-id="4db99-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="4db99-115">Обязательно, если **AuthruleObj** не указан.</span><span class="sxs-lookup"><span data-stu-id="4db99-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db99-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4db99-116">-Confirm</span></span>
<span data-ttu-id="4db99-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4db99-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db99-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db99-118">-WhatIf</span></span>
<span data-ttu-id="4db99-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4db99-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db99-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4db99-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db99-121">-DefaultProfile</span></span>
<span data-ttu-id="4db99-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4db99-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4db99-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="4db99-123">-InputObj</span></span>
<span data-ttu-id="4db99-124">Объект AuthorizationRule пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4db99-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db99-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4db99-125">-Name</span></span>
<span data-ttu-id="4db99-126">AuthorizationRule имя — требуется, если не указан аргумент "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="4db99-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="4db99-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4db99-127">-Namespace</span></span>
<span data-ttu-id="4db99-128">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="4db99-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="4db99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db99-129">CommonParameters</span></span>
<span data-ttu-id="4db99-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4db99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db99-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db99-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db99-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4db99-132">INPUTS</span></span>

### <span data-ttu-id="4db99-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4db99-133">-ResourceGroup</span></span>
 <span data-ttu-id="4db99-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4db99-134">System.String</span></span>

### <span data-ttu-id="4db99-135">-+ +</span><span class="sxs-lookup"><span data-stu-id="4db99-135">-NamespaceName</span></span>
 <span data-ttu-id="4db99-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4db99-136">System.String</span></span>

### <span data-ttu-id="4db99-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="4db99-137">-AuthRuleObj</span></span>
 <span data-ttu-id="4db99-138">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4db99-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4db99-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4db99-139">OUTPUTS</span></span>

### <span data-ttu-id="4db99-140">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4db99-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="4db99-141">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 тип: Microsoft. ServiceBus/AuthorizationRules: AuthoRule1 расположение: Теги: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="4db99-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="4db99-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4db99-142">NOTES</span></span>

## <span data-ttu-id="4db99-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4db99-143">RELATED LINKS</span></span>

