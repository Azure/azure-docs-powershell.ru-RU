---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7074752cda5997bba0536cf891675f59e734e509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556180"
---
# <span data-ttu-id="7cbee-101">New-AddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="7cbee-101">New-AddonPlanDefinitionObject</span></span>

## <span data-ttu-id="7cbee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cbee-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbee-103">Название нужного плана, связанного с предложением или разорвать его связь.</span><span class="sxs-lookup"><span data-stu-id="7cbee-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="7cbee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cbee-104">SYNTAX</span></span>

```
New-AddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="7cbee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cbee-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbee-106">Название нужного плана, связанного с предложением или разорвать его связь.</span><span class="sxs-lookup"><span data-stu-id="7cbee-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="7cbee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cbee-107">EXAMPLES</span></span>

### <span data-ttu-id="7cbee-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7cbee-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="7cbee-109">Создайте новый объект определения плана для указанного плана с ограничением приобретения 500.</span><span class="sxs-lookup"><span data-stu-id="7cbee-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="7cbee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cbee-110">PARAMETERS</span></span>

### <span data-ttu-id="7cbee-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="7cbee-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="7cbee-112">Максимальное количество экземпляров, которое может быть получено одной подпиской.</span><span class="sxs-lookup"><span data-stu-id="7cbee-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="7cbee-113">Если не указано, предполагается значение 1.</span><span class="sxs-lookup"><span data-stu-id="7cbee-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cbee-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="7cbee-114">-PlanId</span></span>
<span data-ttu-id="7cbee-115">Идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="7cbee-115">Plan identifier.</span></span>

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

### <span data-ttu-id="7cbee-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbee-116">CommonParameters</span></span>
<span data-ttu-id="7cbee-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cbee-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbee-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cbee-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbee-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cbee-119">INPUTS</span></span>

## <span data-ttu-id="7cbee-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cbee-120">OUTPUTS</span></span>

## <span data-ttu-id="7cbee-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cbee-121">NOTES</span></span>

## <span data-ttu-id="7cbee-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cbee-122">RELATED LINKS</span></span>

