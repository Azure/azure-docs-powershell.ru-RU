---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562156"
---
# <span data-ttu-id="7b457-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7b457-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="7b457-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b457-102">SYNOPSIS</span></span>
<span data-ttu-id="7b457-103">Удаляет правило авторизации очереди из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="7b457-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b457-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b457-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b457-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b457-105">DESCRIPTION</span></span>
<span data-ttu-id="7b457-106">Командлет **Remove-AzureRmServiceBusQueueAuthorizationRule** удаляет правило авторизации очереди из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="7b457-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7b457-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b457-107">EXAMPLES</span></span>

### <span data-ttu-id="7b457-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b457-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="7b457-109">Удаляет правило авторизации `SBAuthoRule1` очереди `SB-Queue_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7b457-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7b457-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b457-110">PARAMETERS</span></span>

### <span data-ttu-id="7b457-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b457-111">-ResourceGroup</span></span>
<span data-ttu-id="7b457-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b457-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b457-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b457-113">-Confirm</span></span>
<span data-ttu-id="7b457-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b457-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b457-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b457-115">-WhatIf</span></span>
<span data-ttu-id="7b457-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b457-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b457-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b457-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b457-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b457-118">-DefaultProfile</span></span>
<span data-ttu-id="7b457-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b457-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b457-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b457-120">-Name</span></span>
<span data-ttu-id="7b457-121">AuthorizationRule имя очереди.</span><span class="sxs-lookup"><span data-stu-id="7b457-121">Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7b457-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7b457-122">-Namespace</span></span>
<span data-ttu-id="7b457-123">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7b457-123">Namespace Name.</span></span>

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

### <span data-ttu-id="7b457-124">-Очередь</span><span class="sxs-lookup"><span data-stu-id="7b457-124">-Queue</span></span>
<span data-ttu-id="7b457-125">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="7b457-125">Queue Name.</span></span>

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

### <span data-ttu-id="7b457-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b457-126">CommonParameters</span></span>
<span data-ttu-id="7b457-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b457-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b457-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b457-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b457-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b457-129">INPUTS</span></span>

### <span data-ttu-id="7b457-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b457-130">-ResourceGroup</span></span>
 <span data-ttu-id="7b457-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7b457-131">System.String</span></span>

### <span data-ttu-id="7b457-132">-+ +</span><span class="sxs-lookup"><span data-stu-id="7b457-132">-NamespaceName</span></span>
 <span data-ttu-id="7b457-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7b457-133">System.String</span></span>

### <span data-ttu-id="7b457-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="7b457-134">-QueueName</span></span>
 <span data-ttu-id="7b457-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7b457-135">System.String</span></span>

### <span data-ttu-id="7b457-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7b457-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7b457-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7b457-137">System.String</span></span>

## <span data-ttu-id="7b457-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b457-138">OUTPUTS</span></span>

### <span data-ttu-id="7b457-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="7b457-139">System.Object</span></span>

## <span data-ttu-id="7b457-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b457-140">NOTES</span></span>

## <span data-ttu-id="7b457-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b457-141">RELATED LINKS</span></span>

