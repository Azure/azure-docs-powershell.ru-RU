---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908449"
---
# <span data-ttu-id="d8a16-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="d8a16-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="d8a16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8a16-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a16-103">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="d8a16-103">Get the offer metrics.</span></span>

## <span data-ttu-id="d8a16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8a16-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="d8a16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8a16-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a16-106">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="d8a16-106">Get the offer metrics.</span></span>

## <span data-ttu-id="d8a16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8a16-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a16-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8a16-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="d8a16-109">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="d8a16-109">Get the offer metrics.</span></span>

## <span data-ttu-id="d8a16-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8a16-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a16-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="d8a16-111">-OfferName</span></span>
<span data-ttu-id="d8a16-112">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d8a16-112">Name of an offer.</span></span>

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

### <span data-ttu-id="d8a16-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a16-113">-ResourceGroupName</span></span>
<span data-ttu-id="d8a16-114">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="d8a16-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d8a16-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a16-115">CommonParameters</span></span>
<span data-ttu-id="d8a16-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8a16-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a16-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a16-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a16-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8a16-118">INPUTS</span></span>

## <span data-ttu-id="d8a16-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8a16-119">OUTPUTS</span></span>

### <span data-ttu-id="d8a16-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="d8a16-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="d8a16-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8a16-121">NOTES</span></span>

## <span data-ttu-id="d8a16-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8a16-122">RELATED LINKS</span></span>

