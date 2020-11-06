---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 80b3a5ce4cb38222993e69181519a864c578cf67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567914"
---
# <span data-ttu-id="01740-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="01740-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="01740-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01740-102">SYNOPSIS</span></span>
<span data-ttu-id="01740-103">Удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="01740-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01740-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01740-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01740-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01740-105">DESCRIPTION</span></span>
<span data-ttu-id="01740-106">Командлет **Remove-AzureRmServiceBusSubscription** удаляет подписку на раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="01740-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="01740-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01740-107">EXAMPLES</span></span>

### <span data-ttu-id="01740-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01740-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="01740-109">Удаляет подписку `SB-TopicSubscription-Example1` на раздел `SB-Topic_exampl1` в указанном пространстве имен служебной шины `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="01740-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="01740-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01740-110">PARAMETERS</span></span>

### <span data-ttu-id="01740-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01740-111">-DefaultProfile</span></span>
<span data-ttu-id="01740-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01740-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01740-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01740-113">-Name</span></span>
<span data-ttu-id="01740-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="01740-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01740-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="01740-115">-Namespace</span></span>
<span data-ttu-id="01740-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="01740-116">Namespace Name.</span></span>

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

### <span data-ttu-id="01740-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01740-117">-ResourceGroupName</span></span>
<span data-ttu-id="01740-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01740-118">The name of the resource group</span></span>

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

### <span data-ttu-id="01740-119">-Темы</span><span class="sxs-lookup"><span data-stu-id="01740-119">-Topic</span></span>
<span data-ttu-id="01740-120">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="01740-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01740-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01740-121">-Confirm</span></span>
<span data-ttu-id="01740-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01740-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01740-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01740-123">-WhatIf</span></span>
<span data-ttu-id="01740-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01740-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01740-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01740-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01740-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01740-126">CommonParameters</span></span>
<span data-ttu-id="01740-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01740-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01740-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01740-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01740-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01740-129">INPUTS</span></span>

### <span data-ttu-id="01740-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01740-130">-ResourceGroup</span></span>
 <span data-ttu-id="01740-131">System. String</span><span class="sxs-lookup"><span data-stu-id="01740-131">System.String</span></span>

### <span data-ttu-id="01740-132">-+ +</span><span class="sxs-lookup"><span data-stu-id="01740-132">-NamespaceName</span></span>
 <span data-ttu-id="01740-133">System. String</span><span class="sxs-lookup"><span data-stu-id="01740-133">System.String</span></span>

### <span data-ttu-id="01740-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="01740-134">-TopicName</span></span>
 <span data-ttu-id="01740-135">System. String</span><span class="sxs-lookup"><span data-stu-id="01740-135">System.String</span></span>

### <span data-ttu-id="01740-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="01740-136">-SubscriptionName</span></span>
 <span data-ttu-id="01740-137">System. String</span><span class="sxs-lookup"><span data-stu-id="01740-137">System.String</span></span>

## <span data-ttu-id="01740-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01740-138">OUTPUTS</span></span>

### <span data-ttu-id="01740-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01740-139">System.Boolean</span></span>

## <span data-ttu-id="01740-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="01740-140">NOTES</span></span>

## <span data-ttu-id="01740-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01740-141">RELATED LINKS</span></span>

