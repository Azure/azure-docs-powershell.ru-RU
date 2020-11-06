---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555335"
---
# <span data-ttu-id="47682-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="47682-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="47682-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47682-102">SYNOPSIS</span></span>
<span data-ttu-id="47682-103">Название нужного плана, связанного с предложением или разорвать его связь.</span><span class="sxs-lookup"><span data-stu-id="47682-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="47682-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47682-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="47682-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47682-105">DESCRIPTION</span></span>
<span data-ttu-id="47682-106">Название нужного плана, связанного с предложением или разорвать его связь.</span><span class="sxs-lookup"><span data-stu-id="47682-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="47682-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47682-107">EXAMPLES</span></span>

### <span data-ttu-id="47682-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="47682-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="47682-109">Создайте новый объект определения плана для указанного плана с ограничением приобретения 500.</span><span class="sxs-lookup"><span data-stu-id="47682-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="47682-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47682-110">PARAMETERS</span></span>

### <span data-ttu-id="47682-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="47682-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="47682-112">Максимальное количество экземпляров, которое может быть получено одной подпиской.</span><span class="sxs-lookup"><span data-stu-id="47682-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="47682-113">Если не указано, предполагается значение 1.</span><span class="sxs-lookup"><span data-stu-id="47682-113">If not specified, the assumed value is 1.</span></span>

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

### <span data-ttu-id="47682-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="47682-114">-PlanId</span></span>
<span data-ttu-id="47682-115">Идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="47682-115">Plan identifier.</span></span>

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

### <span data-ttu-id="47682-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47682-116">CommonParameters</span></span>
<span data-ttu-id="47682-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47682-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47682-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47682-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47682-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47682-119">INPUTS</span></span>

## <span data-ttu-id="47682-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47682-120">OUTPUTS</span></span>

## <span data-ttu-id="47682-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="47682-121">NOTES</span></span>

## <span data-ttu-id="47682-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47682-122">RELATED LINKS</span></span>

