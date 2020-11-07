---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908762"
---
# <span data-ttu-id="41933-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="41933-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="41933-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41933-102">SYNOPSIS</span></span>
<span data-ttu-id="41933-103">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="41933-103">Get the offer metrics.</span></span>

## <span data-ttu-id="41933-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41933-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="41933-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41933-105">DESCRIPTION</span></span>
<span data-ttu-id="41933-106">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="41933-106">Get the offer metrics.</span></span>

## <span data-ttu-id="41933-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41933-107">EXAMPLES</span></span>

### <span data-ttu-id="41933-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="41933-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="41933-109">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="41933-109">Get the offer metrics.</span></span>

## <span data-ttu-id="41933-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41933-110">PARAMETERS</span></span>

### <span data-ttu-id="41933-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="41933-111">-OfferName</span></span>
<span data-ttu-id="41933-112">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="41933-112">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41933-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41933-113">-ResourceGroupName</span></span>
<span data-ttu-id="41933-114">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="41933-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41933-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41933-115">CommonParameters</span></span>
<span data-ttu-id="41933-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41933-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41933-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41933-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41933-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41933-118">INPUTS</span></span>

## <span data-ttu-id="41933-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41933-119">OUTPUTS</span></span>

### <span data-ttu-id="41933-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="41933-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="41933-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="41933-121">NOTES</span></span>

## <span data-ttu-id="41933-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41933-122">RELATED LINKS</span></span>

