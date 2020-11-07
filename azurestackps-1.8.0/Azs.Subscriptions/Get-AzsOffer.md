---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908369"
---
# <span data-ttu-id="0c120-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="0c120-101">Get-AzsOffer</span></span>

## <span data-ttu-id="0c120-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c120-102">SYNOPSIS</span></span>
<span data-ttu-id="0c120-103">Получите список открытых предложение.</span><span class="sxs-lookup"><span data-stu-id="0c120-103">Get the list of public offers.</span></span>

## <span data-ttu-id="0c120-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c120-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0c120-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c120-105">DESCRIPTION</span></span>
<span data-ttu-id="0c120-106">Получите список открытых предложение.</span><span class="sxs-lookup"><span data-stu-id="0c120-106">Get the list of public offers.</span></span>

## <span data-ttu-id="0c120-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c120-107">EXAMPLES</span></span>

### <span data-ttu-id="0c120-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="0c120-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="0c120-109">Получите список открытых предложение.</span><span class="sxs-lookup"><span data-stu-id="0c120-109">Get the list of public offers.</span></span>

## <span data-ttu-id="0c120-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c120-110">PARAMETERS</span></span>

### <span data-ttu-id="0c120-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="0c120-111">-Skip</span></span>
<span data-ttu-id="0c120-112">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="0c120-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c120-113">-Top</span><span class="sxs-lookup"><span data-stu-id="0c120-113">-Top</span></span>
<span data-ttu-id="0c120-114">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="0c120-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0c120-115">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="0c120-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c120-116">-Provider</span><span class="sxs-lookup"><span data-stu-id="0c120-116">-Provider</span></span>
<span data-ttu-id="0c120-117">Необязательный параметр для указания имени делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="0c120-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="0c120-118">Этот параметр не используется, и его использование будет считаться устаревшим в будущем.</span><span class="sxs-lookup"><span data-stu-id="0c120-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c120-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c120-119">CommonParameters</span></span>
<span data-ttu-id="0c120-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c120-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c120-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c120-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c120-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c120-122">INPUTS</span></span>

## <span data-ttu-id="0c120-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c120-123">OUTPUTS</span></span>

### <span data-ttu-id="0c120-124">Microsoft. AzureStack. Management. Subscription. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="0c120-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="0c120-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c120-125">NOTES</span></span>

## <span data-ttu-id="0c120-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c120-126">RELATED LINKS</span></span>
