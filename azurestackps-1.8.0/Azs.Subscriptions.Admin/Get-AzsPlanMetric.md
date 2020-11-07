---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908446"
---
# <span data-ttu-id="7a0ca-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="7a0ca-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="7a0ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0ca-103">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="7a0ca-103">Get the plan metrics.</span></span>

## <span data-ttu-id="7a0ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a0ca-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="7a0ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0ca-106">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="7a0ca-106">Get the plan metrics.</span></span>

## <span data-ttu-id="7a0ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a0ca-107">EXAMPLES</span></span>

### <span data-ttu-id="7a0ca-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a0ca-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="7a0ca-109">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="7a0ca-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="7a0ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a0ca-110">PARAMETERS</span></span>

### <span data-ttu-id="7a0ca-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7a0ca-111">-PlanName</span></span>
<span data-ttu-id="7a0ca-112">Название плана.</span><span class="sxs-lookup"><span data-stu-id="7a0ca-112">Name of the plan.</span></span>

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

### <span data-ttu-id="7a0ca-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0ca-113">-ResourceGroupName</span></span>
<span data-ttu-id="7a0ca-114">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="7a0ca-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7a0ca-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0ca-115">CommonParameters</span></span>
<span data-ttu-id="7a0ca-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a0ca-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0ca-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0ca-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0ca-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a0ca-118">INPUTS</span></span>

## <span data-ttu-id="7a0ca-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0ca-119">OUTPUTS</span></span>

### <span data-ttu-id="7a0ca-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="7a0ca-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="7a0ca-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a0ca-121">NOTES</span></span>

## <span data-ttu-id="7a0ca-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a0ca-122">RELATED LINKS</span></span>

