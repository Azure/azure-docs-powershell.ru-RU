---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555468"
---
# <span data-ttu-id="c705a-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c705a-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="c705a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c705a-102">SYNOPSIS</span></span>
<span data-ttu-id="c705a-103">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="c705a-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="c705a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c705a-104">SYNTAX</span></span>

### <span data-ttu-id="c705a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c705a-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="c705a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c705a-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="c705a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c705a-107">DESCRIPTION</span></span>
<span data-ttu-id="c705a-108">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="c705a-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="c705a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c705a-109">EXAMPLES</span></span>

### <span data-ttu-id="c705a-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c705a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="c705a-111">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="c705a-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="c705a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c705a-112">PARAMETERS</span></span>

### <span data-ttu-id="c705a-113">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="c705a-113">-Filter</span></span>
<span data-ttu-id="c705a-114">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="c705a-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c705a-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c705a-115">-SubscriptionId</span></span>
<span data-ttu-id="c705a-116">Параметр идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="c705a-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c705a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c705a-117">CommonParameters</span></span>
<span data-ttu-id="c705a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c705a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c705a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c705a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c705a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c705a-120">INPUTS</span></span>

## <span data-ttu-id="c705a-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c705a-121">OUTPUTS</span></span>

### <span data-ttu-id="c705a-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="c705a-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="c705a-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="c705a-123">NOTES</span></span>

## <span data-ttu-id="c705a-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c705a-124">RELATED LINKS</span></span>

