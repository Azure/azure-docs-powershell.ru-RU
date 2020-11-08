---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076689"
---
# <span data-ttu-id="aa3d0-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="aa3d0-101">Get-AzsDisk</span></span>

## <span data-ttu-id="aa3d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3d0-103">Возвращает список управляемых дисков, которые можно перенести в указанном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-103">Returns the list of managed disks which can be migrated in the specified share.</span></span>

## <span data-ttu-id="aa3d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa3d0-104">SYNTAX</span></span>

### <span data-ttu-id="aa3d0-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa3d0-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### <span data-ttu-id="aa3d0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3d0-106">ResourceId</span></span>
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="aa3d0-107">Получить</span><span class="sxs-lookup"><span data-stu-id="aa3d0-107">Get</span></span>
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="aa3d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3d0-108">DESCRIPTION</span></span>
<span data-ttu-id="aa3d0-109">Возвращает список дисков.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-109">Returns a list of disks.</span></span>

## <span data-ttu-id="aa3d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa3d0-110">EXAMPLES</span></span>

### <span data-ttu-id="aa3d0-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa3d0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$disks = Get-AzsDisk -location local
```

<span data-ttu-id="aa3d0-112">Возвращает список управляемых дисков на локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-112">Returns a list of managed disks at the location local.</span></span>
<span data-ttu-id="aa3d0-113">По умолчанию первые диски 100 будут</span><span class="sxs-lookup"><span data-stu-id="aa3d0-113">By default, it will the first 100 disks</span></span>

### <span data-ttu-id="aa3d0-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="aa3d0-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$disk = Get-AzsDisk -location local -name $DiskId
```

<span data-ttu-id="aa3d0-115">Получение определенного управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-115">Get a specific managed disk.</span></span>

## <span data-ttu-id="aa3d0-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa3d0-116">PARAMETERS</span></span>

### <span data-ttu-id="aa3d0-117">— Количество</span><span class="sxs-lookup"><span data-stu-id="aa3d0-117">-Count</span></span>
<span data-ttu-id="aa3d0-118">Максимальное количество возвращаемых дисков.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-118">The maximum number of disks to return.</span></span>

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

### <span data-ttu-id="aa3d0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="aa3d0-119">-Location</span></span>
<span data-ttu-id="aa3d0-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-120">Location of the resource.</span></span>

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

### <span data-ttu-id="aa3d0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa3d0-121">-Name</span></span>
<span data-ttu-id="aa3d0-122">Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-122">The disk guid as identity.</span></span>

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

### <span data-ttu-id="aa3d0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa3d0-123">-ResourceId</span></span>
<span data-ttu-id="aa3d0-124">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-124">The resource id.</span></span>

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

### <span data-ttu-id="aa3d0-125">-SharePath</span><span class="sxs-lookup"><span data-stu-id="aa3d0-125">-SharePath</span></span>
<span data-ttu-id="aa3d0-126">Исходный файл, к которому относится ресурс.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-126">The source share which the resource belongs to.</span></span>

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

### <span data-ttu-id="aa3d0-127">-Start</span><span class="sxs-lookup"><span data-stu-id="aa3d0-127">-Start</span></span>
<span data-ttu-id="aa3d0-128">Начальный индекс дисков в запросе.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-128">The start index of disks in query.</span></span>

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

### <span data-ttu-id="aa3d0-129">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="aa3d0-129">-Status</span></span>
<span data-ttu-id="aa3d0-130">Параметры состояния диска.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-130">The parameters of disk state.</span></span>

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

### <span data-ttu-id="aa3d0-131">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa3d0-131">-UserSubscriptionId</span></span>
<span data-ttu-id="aa3d0-132">Идентификатор подписки клиента, которому принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-132">Tenant Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="aa3d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3d0-133">CommonParameters</span></span>
<span data-ttu-id="aa3d0-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa3d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa3d0-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa3d0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3d0-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa3d0-136">INPUTS</span></span>

## <span data-ttu-id="aa3d0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3d0-137">OUTPUTS</span></span>

### <span data-ttu-id="aa3d0-138">Microsoft. AzureStack. Management. COMPUTE. admin. Model. Disk</span><span class="sxs-lookup"><span data-stu-id="aa3d0-138">Microsoft.AzureStack.Management.Compute.Admin.Models.Disk</span></span>

## <span data-ttu-id="aa3d0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa3d0-139">NOTES</span></span>

## <span data-ttu-id="aa3d0-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa3d0-140">RELATED LINKS</span></span>

