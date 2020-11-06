---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568681"
---
# <span data-ttu-id="bff1d-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bff1d-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="bff1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bff1d-102">SYNOPSIS</span></span>
<span data-ttu-id="bff1d-103">Удаляет правило авторизации для раздела из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bff1d-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bff1d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff1d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff1d-105">DESCRIPTION</span></span>
<span data-ttu-id="bff1d-106">Командлет **Remove-AzureRmServiceBusTopicAuthorizationRule** удаляет правило авторизации для раздела из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="bff1d-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bff1d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bff1d-107">EXAMPLES</span></span>

### <span data-ttu-id="bff1d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bff1d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="bff1d-109">Удаляет правило авторизации `SBTopicAuthoRule1` для раздела `SB-Topic_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="bff1d-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="bff1d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bff1d-110">PARAMETERS</span></span>

### <span data-ttu-id="bff1d-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bff1d-111">-ResourceGroup</span></span>
<span data-ttu-id="bff1d-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bff1d-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="bff1d-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bff1d-113">-Confirm</span></span>
<span data-ttu-id="bff1d-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bff1d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff1d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff1d-115">-WhatIf</span></span>
<span data-ttu-id="bff1d-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bff1d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff1d-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bff1d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff1d-118">-DefaultProfile</span></span>
<span data-ttu-id="bff1d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bff1d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff1d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bff1d-120">-Name</span></span>
<span data-ttu-id="bff1d-121">Название темы AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="bff1d-121">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="bff1d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bff1d-122">-Namespace</span></span>
<span data-ttu-id="bff1d-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="bff1d-123">Namespace Name.</span></span>

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

### <span data-ttu-id="bff1d-124">-Темы</span><span class="sxs-lookup"><span data-stu-id="bff1d-124">-Topic</span></span>
<span data-ttu-id="bff1d-125">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="bff1d-125">Topic Name.</span></span>

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

### <span data-ttu-id="bff1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff1d-126">CommonParameters</span></span>
<span data-ttu-id="bff1d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bff1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff1d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff1d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff1d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bff1d-129">INPUTS</span></span>

### <span data-ttu-id="bff1d-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bff1d-130">-ResourceGroup</span></span>
 <span data-ttu-id="bff1d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bff1d-131">System.String</span></span>

### <span data-ttu-id="bff1d-132">-+ +</span><span class="sxs-lookup"><span data-stu-id="bff1d-132">-NamespaceName</span></span>
 <span data-ttu-id="bff1d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bff1d-133">System.String</span></span>

### <span data-ttu-id="bff1d-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bff1d-134">-TopicName</span></span>
 <span data-ttu-id="bff1d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bff1d-135">System.String</span></span>

### <span data-ttu-id="bff1d-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="bff1d-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="bff1d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bff1d-137">System.String</span></span>

## <span data-ttu-id="bff1d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bff1d-138">OUTPUTS</span></span>

### <span data-ttu-id="bff1d-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="bff1d-139">System.Object</span></span>

## <span data-ttu-id="bff1d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="bff1d-140">NOTES</span></span>

## <span data-ttu-id="bff1d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bff1d-141">RELATED LINKS</span></span>

