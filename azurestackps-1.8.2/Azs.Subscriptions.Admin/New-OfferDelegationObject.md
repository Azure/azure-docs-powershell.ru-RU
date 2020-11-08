---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076753"
---
# <span data-ttu-id="cb286-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="cb286-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="cb286-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb286-102">SYNOPSIS</span></span>
<span data-ttu-id="cb286-103">Делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="cb286-103">Offer delegation.</span></span>

## <span data-ttu-id="cb286-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb286-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="cb286-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb286-105">DESCRIPTION</span></span>
<span data-ttu-id="cb286-106">Делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="cb286-106">Offer delegation.</span></span>

## <span data-ttu-id="cb286-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb286-107">EXAMPLES</span></span>

### <span data-ttu-id="cb286-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb286-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cb286-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="cb286-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cb286-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb286-110">PARAMETERS</span></span>

### <span data-ttu-id="cb286-111">-ID</span><span class="sxs-lookup"><span data-stu-id="cb286-111">-Id</span></span>
<span data-ttu-id="cb286-112">URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb286-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb286-113">-Location</span><span class="sxs-lookup"><span data-stu-id="cb286-113">-Location</span></span>
<span data-ttu-id="cb286-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb286-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb286-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb286-115">-Name</span></span>
<span data-ttu-id="cb286-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb286-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb286-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb286-117">-SubscriptionId</span></span>
<span data-ttu-id="cb286-118">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="cb286-118">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb286-119">-Теги</span><span class="sxs-lookup"><span data-stu-id="cb286-119">-Tags</span></span>
<span data-ttu-id="cb286-120">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="cb286-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb286-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="cb286-121">-Type</span></span>
<span data-ttu-id="cb286-122">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb286-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb286-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb286-123">CommonParameters</span></span>
<span data-ttu-id="cb286-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb286-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb286-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb286-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb286-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb286-126">INPUTS</span></span>

## <span data-ttu-id="cb286-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb286-127">OUTPUTS</span></span>

## <span data-ttu-id="cb286-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb286-128">NOTES</span></span>

## <span data-ttu-id="cb286-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb286-129">RELATED LINKS</span></span>

