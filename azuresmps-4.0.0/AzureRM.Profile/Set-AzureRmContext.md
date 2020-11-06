---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555787"
---
# <span data-ttu-id="f4ad7-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f4ad7-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="f4ad7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ad7-103">Задает клиента, подписку и среду для командлетов, используемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="f4ad7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4ad7-104">SYNTAX</span></span>

### <span data-ttu-id="f4ad7-105">SubscriptionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4ad7-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ad7-106">Context</span><span class="sxs-lookup"><span data-stu-id="f4ad7-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ad7-107">SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4ad7-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ad7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ad7-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ad7-109">Командлет Set-AzureRmContext задает параметры проверки подлинности для командлетов, выполняемых в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="f4ad7-110">Контекст включает сведения о клиенте, подписке и среде.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="f4ad7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4ad7-111">EXAMPLES</span></span>

### <span data-ttu-id="f4ad7-112">Пример 1: Настройка контекста подписки</span><span class="sxs-lookup"><span data-stu-id="f4ad7-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="f4ad7-113">Эта команда задает контекст для использования указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="f4ad7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4ad7-114">PARAMETERS</span></span>

### <span data-ttu-id="f4ad7-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f4ad7-115">-Context</span></span>
<span data-ttu-id="f4ad7-116">Задает контекст для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4ad7-117">-SubscriptionId</span></span>
<span data-ttu-id="f4ad7-118">Указывает идентификатор подписки для контекста, который задает этот командлет для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad7-119">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f4ad7-119">-SubscriptionName</span></span>
<span data-ttu-id="f4ad7-120">Указывает имя подписки для контекста, который задает этот командлет для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad7-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f4ad7-121">-TenantId</span></span>
<span data-ttu-id="f4ad7-122">Указывает идентификатор клиента для контекста, который задает этот командлет для текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4ad7-123">-Confirm</span></span>
<span data-ttu-id="f4ad7-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ad7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ad7-125">-WhatIf</span></span>
<span data-ttu-id="f4ad7-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4ad7-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ad7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ad7-128">CommonParameters</span></span>
<span data-ttu-id="f4ad7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4ad7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ad7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ad7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ad7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4ad7-131">INPUTS</span></span>

## <span data-ttu-id="f4ad7-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4ad7-132">OUTPUTS</span></span>

### <span data-ttu-id="f4ad7-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f4ad7-133">PSAzureContext</span></span>

## <span data-ttu-id="f4ad7-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4ad7-134">NOTES</span></span>

## <span data-ttu-id="f4ad7-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4ad7-135">RELATED LINKS</span></span>

[<span data-ttu-id="f4ad7-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="f4ad7-136">Get-AzureRMContext</span></span>]()

