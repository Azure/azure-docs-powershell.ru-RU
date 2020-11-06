---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4c464d2d0e822b745acc2a7c6daecf329449105
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555400"
---
# <span data-ttu-id="2c231-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="2c231-101">Get-AzsDisk</span></span>

## <span data-ttu-id="2c231-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c231-102">SYNOPSIS</span></span>
<span data-ttu-id="2c231-103">Возвращает список управляемых дисков, которые можно перенести в указанном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="2c231-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="2c231-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c231-104">SYNTAX</span></span>

### <span data-ttu-id="2c231-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c231-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="2c231-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c231-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="2c231-107">Получить</span><span class="sxs-lookup"><span data-stu-id="2c231-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="2c231-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c231-108">DESCRIPTION</span></span>
<span data-ttu-id="2c231-109">Возвращает список дисков.</span><span class="sxs-lookup"><span data-stu-id="2c231-109">Returns a list of disks.</span></span>

## <span data-ttu-id="2c231-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c231-110">EXAMPLES</span></span>

### <span data-ttu-id="2c231-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c231-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="2c231-112">Возвращает список управляемых дисков на локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="2c231-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="2c231-113">По умолчанию первые диски 100 будут</span><span class="sxs-lookup"><span data-stu-id="2c231-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="2c231-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c231-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="2c231-115">Получение определенного управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="2c231-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="2c231-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c231-116">PARAMETERS</span></span>

### <span data-ttu-id="2c231-117">— Количество</span><span class="sxs-lookup"><span data-stu-id="2c231-117">-Count</span></span>
<span data-ttu-id="2c231-118">Максимальное количество возвращаемых дисков.</span><span class="sxs-lookup"><span data-stu-id="2c231-118">The maximum number of disks to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-119">-Location</span><span class="sxs-lookup"><span data-stu-id="2c231-119">-Location</span></span>
<span data-ttu-id="2c231-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c231-120">Location of the resource.</span></span>

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

### <span data-ttu-id="2c231-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c231-121">-Name</span></span>
<span data-ttu-id="2c231-122">Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="2c231-122">The disk guid as identity.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c231-123">-ResourceId</span></span>
<span data-ttu-id="2c231-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2c231-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="2c231-125">-SharePath</span></span>
<span data-ttu-id="2c231-126">Исходный файл, к которому относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="2c231-126">The source share which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-127">-Start</span><span class="sxs-lookup"><span data-stu-id="2c231-127">-Start</span></span>
<span data-ttu-id="2c231-128">Начальный индекс дисков в запросе.</span><span class="sxs-lookup"><span data-stu-id="2c231-128">The start index of disks in query.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-129">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="2c231-129">-Status</span></span>
<span data-ttu-id="2c231-130">Параметры состояния диска.</span><span class="sxs-lookup"><span data-stu-id="2c231-130">The parameters of disk state.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c231-131">-UserSubscriptionId</span></span>
<span data-ttu-id="2c231-132">Идентификатор подписки клиента, которому принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="2c231-132">Tenant Subscription Id which the resource belongs to.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c231-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c231-133">CommonParameters</span></span>
<span data-ttu-id="2c231-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c231-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c231-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c231-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c231-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c231-136">INPUTS</span></span>

## <span data-ttu-id="2c231-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c231-137">OUTPUTS</span></span>

### <span data-ttu-id="2c231-138">Microsoft. AzureStack. Management. COMPUTE. admin. Model. Disk</span><span class="sxs-lookup"><span data-stu-id="2c231-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="2c231-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c231-139">NOTES</span></span>

## <span data-ttu-id="2c231-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c231-140">RELATED LINKS</span></span>

