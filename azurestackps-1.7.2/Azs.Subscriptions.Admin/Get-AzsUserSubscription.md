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
ms.locfileid: "93907914"
---
# <span data-ttu-id="54e22-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="54e22-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="54e22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54e22-102">SYNOPSIS</span></span>
<span data-ttu-id="54e22-103">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="54e22-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="54e22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54e22-104">SYNTAX</span></span>

### <span data-ttu-id="54e22-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54e22-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="54e22-106">Получить</span><span class="sxs-lookup"><span data-stu-id="54e22-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="54e22-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54e22-107">DESCRIPTION</span></span>
<span data-ttu-id="54e22-108">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="54e22-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="54e22-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54e22-109">EXAMPLES</span></span>

### <span data-ttu-id="54e22-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54e22-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="54e22-111">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="54e22-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="54e22-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54e22-112">PARAMETERS</span></span>

### <span data-ttu-id="54e22-113">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="54e22-113">-Filter</span></span>
<span data-ttu-id="54e22-114">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="54e22-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="54e22-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54e22-115">-SubscriptionId</span></span>
<span data-ttu-id="54e22-116">Параметр идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="54e22-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="54e22-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e22-117">CommonParameters</span></span>
<span data-ttu-id="54e22-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54e22-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e22-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e22-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e22-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54e22-120">INPUTS</span></span>

## <span data-ttu-id="54e22-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54e22-121">OUTPUTS</span></span>

### <span data-ttu-id="54e22-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="54e22-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="54e22-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="54e22-123">NOTES</span></span>

## <span data-ttu-id="54e22-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54e22-124">RELATED LINKS</span></span>

