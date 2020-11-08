---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db6eff0b0b0e0698c42dd7905cd3e5f7879345e1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076788"
---
# <span data-ttu-id="907d4-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="907d4-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="907d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="907d4-102">SYNOPSIS</span></span>
<span data-ttu-id="907d4-103">Запускает задание миграции управляемого диска для миграции управляемых дисков в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="907d4-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="907d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="907d4-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="907d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="907d4-105">DESCRIPTION</span></span>
<span data-ttu-id="907d4-106">Создание задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="907d4-106">Create a disk migration job.</span></span>

## <span data-ttu-id="907d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="907d4-107">EXAMPLES</span></span>

### <span data-ttu-id="907d4-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="907d4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="907d4-109">Запуск задания миграции управляемого диска для первых 20 дисков</span><span class="sxs-lookup"><span data-stu-id="907d4-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="907d4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="907d4-110">PARAMETERS</span></span>

### <span data-ttu-id="907d4-111">-Диски</span><span class="sxs-lookup"><span data-stu-id="907d4-111">-Disks</span></span>
<span data-ttu-id="907d4-112">Параметры списка дисков.</span><span class="sxs-lookup"><span data-stu-id="907d4-112">The parameters of disk list.</span></span>

```yaml
Type: Disk[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907d4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="907d4-113">-Location</span></span>
<span data-ttu-id="907d4-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="907d4-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907d4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="907d4-115">-Name</span></span>
<span data-ttu-id="907d4-116">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="907d4-116">The migration job guid name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907d4-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="907d4-117">-TargetShare</span></span>
<span data-ttu-id="907d4-118">Имя целевого общего доступа.</span><span class="sxs-lookup"><span data-stu-id="907d4-118">The target share name.</span></span>

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

### <span data-ttu-id="907d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907d4-119">CommonParameters</span></span>
<span data-ttu-id="907d4-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="907d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="907d4-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="907d4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907d4-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="907d4-122">INPUTS</span></span>

## <span data-ttu-id="907d4-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="907d4-123">OUTPUTS</span></span>

### <span data-ttu-id="907d4-124">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="907d4-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="907d4-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="907d4-125">NOTES</span></span>

## <span data-ttu-id="907d4-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="907d4-126">RELATED LINKS</span></span>

