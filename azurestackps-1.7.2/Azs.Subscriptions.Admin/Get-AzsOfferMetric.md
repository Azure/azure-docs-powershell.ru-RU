---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907890"
---
# <span data-ttu-id="f600c-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="f600c-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="f600c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f600c-102">SYNOPSIS</span></span>
<span data-ttu-id="f600c-103">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="f600c-103">Get the offer metrics.</span></span>

## <span data-ttu-id="f600c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f600c-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="f600c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f600c-105">DESCRIPTION</span></span>
<span data-ttu-id="f600c-106">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="f600c-106">Get the offer metrics.</span></span>

## <span data-ttu-id="f600c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f600c-107">EXAMPLES</span></span>

### <span data-ttu-id="f600c-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f600c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="f600c-109">Получение метрик предложения.</span><span class="sxs-lookup"><span data-stu-id="f600c-109">Get the offer metrics.</span></span>

## <span data-ttu-id="f600c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f600c-110">PARAMETERS</span></span>

### <span data-ttu-id="f600c-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="f600c-111">-OfferName</span></span>
<span data-ttu-id="f600c-112">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="f600c-112">Name of an offer.</span></span>

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

### <span data-ttu-id="f600c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f600c-113">-ResourceGroupName</span></span>
<span data-ttu-id="f600c-114">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="f600c-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f600c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f600c-115">CommonParameters</span></span>
<span data-ttu-id="f600c-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f600c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f600c-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f600c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f600c-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f600c-118">INPUTS</span></span>

## <span data-ttu-id="f600c-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f600c-119">OUTPUTS</span></span>

### <span data-ttu-id="f600c-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="f600c-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="f600c-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="f600c-121">NOTES</span></span>

## <span data-ttu-id="f600c-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f600c-122">RELATED LINKS</span></span>

