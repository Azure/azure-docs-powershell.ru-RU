---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731725"
---
# <span data-ttu-id="79505-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="79505-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="79505-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79505-102">SYNOPSIS</span></span>
<span data-ttu-id="79505-103">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="79505-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="79505-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79505-104">SYNTAX</span></span>

### <span data-ttu-id="79505-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79505-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="79505-106">Получить</span><span class="sxs-lookup"><span data-stu-id="79505-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="79505-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="79505-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="79505-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79505-108">DESCRIPTION</span></span>
<span data-ttu-id="79505-109">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="79505-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="79505-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79505-110">EXAMPLES</span></span>

### <span data-ttu-id="79505-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="79505-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="79505-112">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="79505-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="79505-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="79505-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="79505-114">Возвращает состояние работоспособности под заголовком "для Microsoft. Fabric. admin".</span><span class="sxs-lookup"><span data-stu-id="79505-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="79505-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79505-115">PARAMETERS</span></span>

### <span data-ttu-id="79505-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="79505-116">-Filter</span></span>
<span data-ttu-id="79505-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="79505-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="79505-118">-Location</span><span class="sxs-lookup"><span data-stu-id="79505-118">-Location</span></span>
<span data-ttu-id="79505-119">Название региона</span><span class="sxs-lookup"><span data-stu-id="79505-119">Name of the region</span></span>

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

### <span data-ttu-id="79505-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79505-120">-Name</span></span>
<span data-ttu-id="79505-121">Название ресурса объекта работоспособности, соответствующего идентификатору регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="79505-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79505-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79505-122">-ResourceGroupName</span></span>
<span data-ttu-id="79505-123">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="79505-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="79505-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79505-124">-ResourceId</span></span>
<span data-ttu-id="79505-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="79505-125">The resource id.</span></span>

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

### <span data-ttu-id="79505-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="79505-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="79505-127">Регистрационный код службы.</span><span class="sxs-lookup"><span data-stu-id="79505-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79505-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="79505-128">-Skip</span></span>
<span data-ttu-id="79505-129">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="79505-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="79505-130">-Top</span><span class="sxs-lookup"><span data-stu-id="79505-130">-Top</span></span>
<span data-ttu-id="79505-131">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="79505-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="79505-132">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="79505-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="79505-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79505-133">CommonParameters</span></span>
<span data-ttu-id="79505-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79505-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79505-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79505-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79505-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79505-136">INPUTS</span></span>

## <span data-ttu-id="79505-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79505-137">OUTPUTS</span></span>

### <span data-ttu-id="79505-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ResourceHealth</span><span class="sxs-lookup"><span data-stu-id="79505-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="79505-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="79505-139">NOTES</span></span>

## <span data-ttu-id="79505-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79505-140">RELATED LINKS</span></span>

