---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cf36bf232ae48891b28562313fa2063e14a2be8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906750"
---
# <span data-ttu-id="72c18-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="72c18-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="72c18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72c18-102">SYNOPSIS</span></span>
<span data-ttu-id="72c18-103">Возвращает список управляемых задач миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="72c18-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="72c18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72c18-104">SYNTAX</span></span>

### <span data-ttu-id="72c18-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72c18-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="72c18-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c18-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="72c18-107">Получить</span><span class="sxs-lookup"><span data-stu-id="72c18-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="72c18-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72c18-108">DESCRIPTION</span></span>
<span data-ttu-id="72c18-109">Возвращает список заданий миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="72c18-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="72c18-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72c18-110">EXAMPLES</span></span>

### <span data-ttu-id="72c18-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="72c18-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="72c18-112">Получение определенного задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="72c18-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="72c18-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="72c18-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="72c18-114">Возвращает список управляемых заданий миграции дисков на локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="72c18-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="72c18-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72c18-115">PARAMETERS</span></span>

### <span data-ttu-id="72c18-116">-Location</span><span class="sxs-lookup"><span data-stu-id="72c18-116">-Location</span></span>
<span data-ttu-id="72c18-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="72c18-117">Location of the resource.</span></span>

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

### <span data-ttu-id="72c18-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72c18-118">-Name</span></span>
<span data-ttu-id="72c18-119">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="72c18-119">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72c18-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c18-120">-ResourceId</span></span>
<span data-ttu-id="72c18-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="72c18-121">The resource id.</span></span>

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

### <span data-ttu-id="72c18-122">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="72c18-122">-Status</span></span>
<span data-ttu-id="72c18-123">Параметры состояния задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="72c18-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="72c18-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c18-124">CommonParameters</span></span>
<span data-ttu-id="72c18-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72c18-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c18-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c18-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c18-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72c18-127">INPUTS</span></span>

## <span data-ttu-id="72c18-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72c18-128">OUTPUTS</span></span>

### <span data-ttu-id="72c18-129">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="72c18-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="72c18-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="72c18-130">NOTES</span></span>

## <span data-ttu-id="72c18-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72c18-131">RELATED LINKS</span></span>

