---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076985"
---
# <span data-ttu-id="e387a-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="e387a-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="e387a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e387a-102">SYNOPSIS</span></span>
<span data-ttu-id="e387a-103">Получите список подписок пользователей в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="e387a-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="e387a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e387a-104">SYNTAX</span></span>

### <span data-ttu-id="e387a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e387a-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="e387a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e387a-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="e387a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e387a-107">DESCRIPTION</span></span>
<span data-ttu-id="e387a-108">Получите список подписок пользователей в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="e387a-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="e387a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e387a-109">EXAMPLES</span></span>

### <span data-ttu-id="e387a-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e387a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="e387a-111">Получите список подписок пользователей в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="e387a-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="e387a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e387a-112">PARAMETERS</span></span>

### <span data-ttu-id="e387a-113">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="e387a-113">-Filter</span></span>
<span data-ttu-id="e387a-114">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="e387a-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="e387a-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e387a-115">-SubscriptionId</span></span>
<span data-ttu-id="e387a-116">Параметр идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="e387a-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="e387a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e387a-117">CommonParameters</span></span>
<span data-ttu-id="e387a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e387a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e387a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e387a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e387a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e387a-120">INPUTS</span></span>

## <span data-ttu-id="e387a-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e387a-121">OUTPUTS</span></span>

### <span data-ttu-id="e387a-122">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="e387a-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="e387a-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e387a-123">NOTES</span></span>

## <span data-ttu-id="e387a-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e387a-124">RELATED LINKS</span></span>

