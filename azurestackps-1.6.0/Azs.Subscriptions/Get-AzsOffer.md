---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556111"
---
# <span data-ttu-id="7b723-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="7b723-101">Get-AzsOffer</span></span>

## <span data-ttu-id="7b723-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b723-102">SYNOPSIS</span></span>
<span data-ttu-id="7b723-103">Получите список открытых предложение.</span><span class="sxs-lookup"><span data-stu-id="7b723-103">Get the list of public offers.</span></span>

## <span data-ttu-id="7b723-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b723-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7b723-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b723-105">DESCRIPTION</span></span>
<span data-ttu-id="7b723-106">Получите список открытых предложение.</span><span class="sxs-lookup"><span data-stu-id="7b723-106">Get the list of public offers.</span></span>

## <span data-ttu-id="7b723-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b723-107">EXAMPLES</span></span>

### <span data-ttu-id="7b723-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7b723-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="7b723-109">Получите список открытых предложение.</span><span class="sxs-lookup"><span data-stu-id="7b723-109">Get the list of public offers.</span></span>

## <span data-ttu-id="7b723-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b723-110">PARAMETERS</span></span>

### <span data-ttu-id="7b723-111">-Skip</span><span class="sxs-lookup"><span data-stu-id="7b723-111">-Skip</span></span>
<span data-ttu-id="7b723-112">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="7b723-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7b723-113">-Top</span><span class="sxs-lookup"><span data-stu-id="7b723-113">-Top</span></span>
<span data-ttu-id="7b723-114">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="7b723-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7b723-115">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="7b723-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7b723-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b723-116">CommonParameters</span></span>
<span data-ttu-id="7b723-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b723-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b723-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b723-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b723-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b723-119">INPUTS</span></span>

## <span data-ttu-id="7b723-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b723-120">OUTPUTS</span></span>

### <span data-ttu-id="7b723-121">Microsoft. AzureStack. Management. Subscription. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="7b723-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="7b723-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b723-122">NOTES</span></span>

## <span data-ttu-id="7b723-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b723-123">RELATED LINKS</span></span>

