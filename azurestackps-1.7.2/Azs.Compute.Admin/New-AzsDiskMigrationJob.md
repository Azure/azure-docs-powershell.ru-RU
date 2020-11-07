---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcbc31b31558a38e61648a0eb9318f68daf19d2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907922"
---
# <span data-ttu-id="61706-101">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="61706-101">New-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="61706-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61706-102">SYNOPSIS</span></span>
<span data-ttu-id="61706-103">Запускает задание миграции управляемого диска для миграции управляемых дисков в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="61706-103">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

## <span data-ttu-id="61706-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61706-104">SYNTAX</span></span>

```
New-AzsDiskMigrationJob [-Disks] <Disk[]> [-TargetShare] <String> [[-Location] <String>] [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="61706-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61706-105">DESCRIPTION</span></span>
<span data-ttu-id="61706-106">Создание задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="61706-106">Create a disk migration job.</span></span>

## <span data-ttu-id="61706-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61706-107">EXAMPLES</span></span>

### <span data-ttu-id="61706-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61706-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsDiskMigrationJob -Name "MyMigrationJob" -Disks $disks -location local -TargetShare "\\SU1FileServer.azurestack.local\SU1_ObjStore"
```

<span data-ttu-id="61706-109">Запуск задания миграции управляемого диска для первых 20 дисков</span><span class="sxs-lookup"><span data-stu-id="61706-109">Start a managed disk migration job for the first 20 disks</span></span>

## <span data-ttu-id="61706-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61706-110">PARAMETERS</span></span>

### <span data-ttu-id="61706-111">-Диски</span><span class="sxs-lookup"><span data-stu-id="61706-111">-Disks</span></span>
<span data-ttu-id="61706-112">Параметры списка дисков.</span><span class="sxs-lookup"><span data-stu-id="61706-112">The parameters of disk list.</span></span>

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

### <span data-ttu-id="61706-113">-Location</span><span class="sxs-lookup"><span data-stu-id="61706-113">-Location</span></span>
<span data-ttu-id="61706-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="61706-114">Location of the resource.</span></span>

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

### <span data-ttu-id="61706-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61706-115">-Name</span></span>
<span data-ttu-id="61706-116">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="61706-116">The migration job guid name.</span></span>

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

### <span data-ttu-id="61706-117">-TargetShare</span><span class="sxs-lookup"><span data-stu-id="61706-117">-TargetShare</span></span>
<span data-ttu-id="61706-118">Имя целевого общего доступа.</span><span class="sxs-lookup"><span data-stu-id="61706-118">The target share name.</span></span>

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

### <span data-ttu-id="61706-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61706-119">CommonParameters</span></span>
<span data-ttu-id="61706-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61706-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61706-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61706-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61706-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61706-122">INPUTS</span></span>

## <span data-ttu-id="61706-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61706-123">OUTPUTS</span></span>

### <span data-ttu-id="61706-124">Microsoft. AzureStack. Management. COMPUTE. admin. Models. DiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="61706-124">Microsoft.AzureStack.Management.Compute.Admin.Models.DiskMigrationJob</span></span>

## <span data-ttu-id="61706-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="61706-125">NOTES</span></span>

## <span data-ttu-id="61706-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61706-126">RELATED LINKS</span></span>

