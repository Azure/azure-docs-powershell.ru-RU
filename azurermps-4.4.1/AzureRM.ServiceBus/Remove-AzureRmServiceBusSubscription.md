---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562148"
---
# <span data-ttu-id="dec29-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="dec29-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="dec29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dec29-102">SYNOPSIS</span></span>
<span data-ttu-id="dec29-103">Удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="dec29-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dec29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dec29-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dec29-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dec29-105">DESCRIPTION</span></span>
<span data-ttu-id="dec29-106">Командлет **Remove-AzureRmServiceBusSubscription** удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="dec29-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="dec29-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dec29-107">EXAMPLES</span></span>

### <span data-ttu-id="dec29-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dec29-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="dec29-109">Удаляет подписку `SB-TopicSubscription-Example1` на раздел `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="dec29-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="dec29-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dec29-110">PARAMETERS</span></span>

### <span data-ttu-id="dec29-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dec29-111">-Confirm</span></span>
<span data-ttu-id="dec29-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dec29-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dec29-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dec29-113">-WhatIf</span></span>
<span data-ttu-id="dec29-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dec29-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dec29-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dec29-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dec29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec29-116">-DefaultProfile</span></span>
<span data-ttu-id="dec29-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dec29-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dec29-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dec29-118">-Name</span></span>
<span data-ttu-id="dec29-119">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="dec29-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec29-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dec29-120">-Namespace</span></span>
<span data-ttu-id="dec29-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dec29-121">Namespace Name.</span></span>

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

### <span data-ttu-id="dec29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec29-122">-ResourceGroupName</span></span>
<span data-ttu-id="dec29-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dec29-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dec29-124">-Темы</span><span class="sxs-lookup"><span data-stu-id="dec29-124">-Topic</span></span>
<span data-ttu-id="dec29-125">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="dec29-125">Topic Name.</span></span>

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

### <span data-ttu-id="dec29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec29-126">CommonParameters</span></span>
<span data-ttu-id="dec29-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dec29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec29-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec29-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec29-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dec29-129">INPUTS</span></span>

### <span data-ttu-id="dec29-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dec29-130">-ResourceGroup</span></span>
 <span data-ttu-id="dec29-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dec29-131">System.String</span></span>

### <span data-ttu-id="dec29-132">-+ +</span><span class="sxs-lookup"><span data-stu-id="dec29-132">-NamespaceName</span></span>
 <span data-ttu-id="dec29-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dec29-133">System.String</span></span>

### <span data-ttu-id="dec29-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="dec29-134">-TopicName</span></span>
 <span data-ttu-id="dec29-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dec29-135">System.String</span></span>

### <span data-ttu-id="dec29-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="dec29-136">-SubscriptionName</span></span>
 <span data-ttu-id="dec29-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dec29-137">System.String</span></span>

## <span data-ttu-id="dec29-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dec29-138">OUTPUTS</span></span>

### <span data-ttu-id="dec29-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dec29-139">System.Boolean</span></span>

## <span data-ttu-id="dec29-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="dec29-140">NOTES</span></span>

## <span data-ttu-id="dec29-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dec29-141">RELATED LINKS</span></span>

