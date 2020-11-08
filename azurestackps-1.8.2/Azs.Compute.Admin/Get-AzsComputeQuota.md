---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076696"
---
# <span data-ttu-id="04f95-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="04f95-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="04f95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04f95-102">SYNOPSIS</span></span>
<span data-ttu-id="04f95-103">Возвращает квоты с указанием предельных квот для вычисляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="04f95-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="04f95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04f95-104">SYNTAX</span></span>

### <span data-ttu-id="04f95-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04f95-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="04f95-106">Получить</span><span class="sxs-lookup"><span data-stu-id="04f95-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="04f95-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="04f95-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="04f95-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04f95-108">DESCRIPTION</span></span>
<span data-ttu-id="04f95-109">Получение списка существующих квот.</span><span class="sxs-lookup"><span data-stu-id="04f95-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="04f95-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04f95-110">EXAMPLES</span></span>

### <span data-ttu-id="04f95-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="04f95-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="04f95-112">Получить все расчетные квоты в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="04f95-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="04f95-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="04f95-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="04f95-114">Получить определенную расчетную квоту.</span><span class="sxs-lookup"><span data-stu-id="04f95-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="04f95-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04f95-115">PARAMETERS</span></span>

### <span data-ttu-id="04f95-116">-Location</span><span class="sxs-lookup"><span data-stu-id="04f95-116">-Location</span></span>
<span data-ttu-id="04f95-117">{{Описание расположения заливки}}</span><span class="sxs-lookup"><span data-stu-id="04f95-117">{{Fill Location Description}}</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f95-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04f95-118">-Name</span></span>
<span data-ttu-id="04f95-119">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="04f95-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f95-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04f95-120">-ResourceId</span></span>
<span data-ttu-id="04f95-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="04f95-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f95-122">CommonParameters</span></span>
<span data-ttu-id="04f95-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04f95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f95-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f95-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f95-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04f95-125">INPUTS</span></span>

## <span data-ttu-id="04f95-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04f95-126">OUTPUTS</span></span>

### <span data-ttu-id="04f95-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="04f95-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="04f95-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="04f95-128">NOTES</span></span>

## <span data-ttu-id="04f95-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04f95-129">RELATED LINKS</span></span>

