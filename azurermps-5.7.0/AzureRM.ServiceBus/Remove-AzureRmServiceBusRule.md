---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566109"
---
# <span data-ttu-id="4086d-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4086d-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4086d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4086d-102">SYNOPSIS</span></span>
<span data-ttu-id="4086d-103">Удаляет правило speficied для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="4086d-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4086d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4086d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4086d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4086d-105">DESCRIPTION</span></span>
<span data-ttu-id="4086d-106">Командлет **Remove-AzureRmServiceBusRule** удаляет правило подписки на данную тему.</span><span class="sxs-lookup"><span data-stu-id="4086d-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="4086d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4086d-107">EXAMPLES</span></span>

### <span data-ttu-id="4086d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4086d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="4086d-109">Удаляет правило `SBRule` подписки `SBSubscription` для указанной темы `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="4086d-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="4086d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4086d-110">PARAMETERS</span></span>

### <span data-ttu-id="4086d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4086d-111">-DefaultProfile</span></span>
<span data-ttu-id="4086d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4086d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4086d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4086d-113">-Force</span></span>
<span data-ttu-id="4086d-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4086d-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4086d-115">-Name</span></span>
<span data-ttu-id="4086d-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="4086d-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4086d-117">-Namespace</span></span>
<span data-ttu-id="4086d-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4086d-118">Namespace Name.</span></span>

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

### <span data-ttu-id="4086d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4086d-119">-PassThru</span></span>
<span data-ttu-id="4086d-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="4086d-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4086d-121">-ResourceGroupName</span></span>
<span data-ttu-id="4086d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4086d-122">The name of the resource group</span></span>

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

### <span data-ttu-id="4086d-123">-Подписка</span><span class="sxs-lookup"><span data-stu-id="4086d-123">-Subscription</span></span>
<span data-ttu-id="4086d-124">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="4086d-124">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-125">-Темы</span><span class="sxs-lookup"><span data-stu-id="4086d-125">-Topic</span></span>
<span data-ttu-id="4086d-126">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="4086d-126">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4086d-127">-Confirm</span></span>
<span data-ttu-id="4086d-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4086d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4086d-129">-WhatIf</span></span>
<span data-ttu-id="4086d-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4086d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4086d-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4086d-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4086d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4086d-132">CommonParameters</span></span>
<span data-ttu-id="4086d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4086d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4086d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4086d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4086d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4086d-135">INPUTS</span></span>

### <span data-ttu-id="4086d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4086d-136">System.String</span></span>

## <span data-ttu-id="4086d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4086d-137">OUTPUTS</span></span>

### <span data-ttu-id="4086d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4086d-138">System.Boolean</span></span>

## <span data-ttu-id="4086d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4086d-139">NOTES</span></span>

## <span data-ttu-id="4086d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4086d-140">RELATED LINKS</span></span>

