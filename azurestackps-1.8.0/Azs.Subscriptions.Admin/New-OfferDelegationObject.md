---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908409"
---
# <span data-ttu-id="fc983-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="fc983-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="fc983-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc983-102">SYNOPSIS</span></span>
<span data-ttu-id="fc983-103">Делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="fc983-103">Offer delegation.</span></span>

## <span data-ttu-id="fc983-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc983-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="fc983-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc983-105">DESCRIPTION</span></span>
<span data-ttu-id="fc983-106">Делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="fc983-106">Offer delegation.</span></span>

## <span data-ttu-id="fc983-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc983-107">EXAMPLES</span></span>

### <span data-ttu-id="fc983-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc983-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fc983-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="fc983-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="fc983-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc983-110">PARAMETERS</span></span>

### <span data-ttu-id="fc983-111">-ID</span><span class="sxs-lookup"><span data-stu-id="fc983-111">-Id</span></span>
<span data-ttu-id="fc983-112">URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc983-112">URI of the resource.</span></span>

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

### <span data-ttu-id="fc983-113">-Location</span><span class="sxs-lookup"><span data-stu-id="fc983-113">-Location</span></span>
<span data-ttu-id="fc983-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc983-114">Location of the resource.</span></span>

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

### <span data-ttu-id="fc983-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc983-115">-Name</span></span>
<span data-ttu-id="fc983-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc983-116">Name of the resource.</span></span>

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

### <span data-ttu-id="fc983-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc983-117">-SubscriptionId</span></span>
<span data-ttu-id="fc983-118">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="fc983-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="fc983-119">-Теги</span><span class="sxs-lookup"><span data-stu-id="fc983-119">-Tags</span></span>
<span data-ttu-id="fc983-120">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="fc983-120">List of key-value pairs.</span></span>

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

### <span data-ttu-id="fc983-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="fc983-121">-Type</span></span>
<span data-ttu-id="fc983-122">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc983-122">Type of resource.</span></span>

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

### <span data-ttu-id="fc983-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc983-123">CommonParameters</span></span>
<span data-ttu-id="fc983-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc983-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc983-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc983-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc983-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc983-126">INPUTS</span></span>

## <span data-ttu-id="fc983-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc983-127">OUTPUTS</span></span>

## <span data-ttu-id="fc983-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc983-128">NOTES</span></span>

## <span data-ttu-id="fc983-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc983-129">RELATED LINKS</span></span>

