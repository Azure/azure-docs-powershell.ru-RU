---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908918"
---
# <span data-ttu-id="3b13c-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="3b13c-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="3b13c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b13c-102">SYNOPSIS</span></span>
<span data-ttu-id="3b13c-103">Возвращает список управляемых задач миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="3b13c-103">Returns the list of managed disk migration jobs.</span></span>

## <span data-ttu-id="3b13c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b13c-104">SYNTAX</span></span>

### <span data-ttu-id="3b13c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b13c-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="3b13c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b13c-106">ResourceId</span></span>
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="3b13c-107">Получить</span><span class="sxs-lookup"><span data-stu-id="3b13c-107">Get</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## <span data-ttu-id="3b13c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b13c-108">DESCRIPTION</span></span>
<span data-ttu-id="3b13c-109">Возвращает список заданий миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="3b13c-109">Returns a list of disk migration jobs.</span></span>

## <span data-ttu-id="3b13c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b13c-110">EXAMPLES</span></span>

### <span data-ttu-id="3b13c-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b13c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

<span data-ttu-id="3b13c-112">Получение определенного задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="3b13c-112">Get a specific managed disk migration job.</span></span>

### <span data-ttu-id="3b13c-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b13c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
$migration = Get-AzsDiskMigrationJob -location local
```

<span data-ttu-id="3b13c-114">Возвращает список управляемых заданий миграции дисков на локальном расположении.</span><span class="sxs-lookup"><span data-stu-id="3b13c-114">Returns a list of managed disk migration jobs at the location local.</span></span>

## <span data-ttu-id="3b13c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b13c-115">PARAMETERS</span></span>

### <span data-ttu-id="3b13c-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3b13c-116">-Location</span></span>
<span data-ttu-id="3b13c-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b13c-117">Location of the resource.</span></span>

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

### <span data-ttu-id="3b13c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b13c-118">-Name</span></span>
<span data-ttu-id="3b13c-119">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="3b13c-119">The migration job guid name.</span></span>

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

### <span data-ttu-id="3b13c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b13c-120">-ResourceId</span></span>
<span data-ttu-id="3b13c-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b13c-121">The resource id.</span></span>

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

### <span data-ttu-id="3b13c-122">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="3b13c-122">-Status</span></span>
<span data-ttu-id="3b13c-123">Параметры состояния задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="3b13c-123">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="3b13c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b13c-124">CommonParameters</span></span>
<span data-ttu-id="3b13c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b13c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b13c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b13c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b13c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b13c-127">INPUTS</span></span>

## <span data-ttu-id="3b13c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b13c-128">OUTPUTS</span></span>

### <span data-ttu-id="3b13c-129">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="3b13c-129">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="3b13c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b13c-130">NOTES</span></span>

## <span data-ttu-id="3b13c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b13c-131">RELATED LINKS</span></span>

