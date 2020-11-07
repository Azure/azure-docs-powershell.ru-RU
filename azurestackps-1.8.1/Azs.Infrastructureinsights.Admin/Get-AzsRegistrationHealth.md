---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909106"
---
# <span data-ttu-id="379f2-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="379f2-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="379f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="379f2-102">SYNOPSIS</span></span>
<span data-ttu-id="379f2-103">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="379f2-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="379f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="379f2-104">SYNTAX</span></span>

### <span data-ttu-id="379f2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="379f2-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="379f2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="379f2-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="379f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="379f2-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="379f2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="379f2-108">DESCRIPTION</span></span>
<span data-ttu-id="379f2-109">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="379f2-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="379f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="379f2-110">EXAMPLES</span></span>

### <span data-ttu-id="379f2-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="379f2-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="379f2-112">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="379f2-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="379f2-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="379f2-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="379f2-114">Возвращает состояние работоспособности под заголовком "для Microsoft. Fabric. admin".</span><span class="sxs-lookup"><span data-stu-id="379f2-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="379f2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="379f2-115">PARAMETERS</span></span>

### <span data-ttu-id="379f2-116">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="379f2-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="379f2-117">Регистрационный код службы.</span><span class="sxs-lookup"><span data-stu-id="379f2-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379f2-118">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="379f2-118">-ResourceRegistrationId</span></span>


```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379f2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="379f2-119">-Location</span></span>
<span data-ttu-id="379f2-120">Название региона</span><span class="sxs-lookup"><span data-stu-id="379f2-120">Name of the region</span></span>

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

### <span data-ttu-id="379f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="379f2-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="379f2-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="379f2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="379f2-123">-ResourceId</span></span>
<span data-ttu-id="379f2-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="379f2-124">The resource id.</span></span>

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

### <span data-ttu-id="379f2-125">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="379f2-125">-Filter</span></span>
<span data-ttu-id="379f2-126">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="379f2-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379f2-127">-Top</span><span class="sxs-lookup"><span data-stu-id="379f2-127">-Top</span></span>
<span data-ttu-id="379f2-128">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="379f2-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="379f2-129">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="379f2-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379f2-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="379f2-130">-Skip</span></span>
<span data-ttu-id="379f2-131">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="379f2-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379f2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379f2-132">CommonParameters</span></span>
<span data-ttu-id="379f2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="379f2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379f2-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="379f2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379f2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="379f2-135">INPUTS</span></span>

## <span data-ttu-id="379f2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="379f2-136">OUTPUTS</span></span>

### <span data-ttu-id="379f2-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="379f2-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="379f2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="379f2-138">NOTES</span></span>

## <span data-ttu-id="379f2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="379f2-139">RELATED LINKS</span></span>
