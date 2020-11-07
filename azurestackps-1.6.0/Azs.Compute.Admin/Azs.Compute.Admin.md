---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 4194899ad20356c8cde68110553495558d3816d5
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719749"
---
# <span data-ttu-id="5cb78-101">Модуль AZS. COMPUTE. администратора</span><span class="sxs-lookup"><span data-stu-id="5cb78-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="5cb78-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="5cb78-102">Description</span></span>
<span data-ttu-id="5cb78-103">Предварительный просмотр выпуска модуля оператора вычисления AzureStack, который предоставляет функциональные возможности для управления вычислительными квотами, изображениями платформы и расширениями виртуальных машин, а также заданиями миграции управляемых дисков для повторной балансировки хранилища.</span><span class="sxs-lookup"><span data-stu-id="5cb78-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="5cb78-104">Командлеты AZS. COMPUTE. администратора</span><span class="sxs-lookup"><span data-stu-id="5cb78-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="5cb78-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5cb78-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="5cb78-106">Добавление образа платформы виртуальной машины из заданной конфигурации образа.</span><span class="sxs-lookup"><span data-stu-id="5cb78-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="5cb78-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="5cb78-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="5cb78-108">Создайте новый образ расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5cb78-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="5cb78-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5cb78-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="5cb78-110">Возвращает квоты с указанием предельных квот для вычисляемых объектов.</span><span class="sxs-lookup"><span data-stu-id="5cb78-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="5cb78-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="5cb78-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="5cb78-112">Возвращает список управляемых дисков, которые можно перенести в указанном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="5cb78-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="5cb78-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="5cb78-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="5cb78-114">Возвращает список управляемых задач миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="5cb78-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="5cb78-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5cb78-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="5cb78-116">Возвращает образы виртуальных машин, загруженные в репозиторий образов платформы.</span><span class="sxs-lookup"><span data-stu-id="5cb78-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="5cb78-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="5cb78-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="5cb78-118">Возвращает доступ к расширениям изображений виртуальной машины в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="5cb78-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="5cb78-119">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5cb78-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="5cb78-120">Создайте новую вычислительную квоту, используемую для ограничения вычислительных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cb78-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="5cb78-121">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="5cb78-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="5cb78-122">Запускает задание миграции управляемого диска для миграции управляемых дисков в указанную конечную папку.</span><span class="sxs-lookup"><span data-stu-id="5cb78-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="5cb78-123">New-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="5cb78-123">New-AzsDataDiskObject</span></span>](New-AzsDataDiskObject.md)
<span data-ttu-id="5cb78-124">Создание диска данных, который используется для создания нового образа платформы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5cb78-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="5cb78-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5cb78-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="5cb78-126">Удаляет указанную вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="5cb78-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="5cb78-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="5cb78-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="5cb78-128">Удаление образа виртуальной машины из репозитория образов платформы.</span><span class="sxs-lookup"><span data-stu-id="5cb78-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="5cb78-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="5cb78-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="5cb78-130">Удаляет изображение расширения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5cb78-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="5cb78-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="5cb78-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="5cb78-132">Обновите существующую вычислительную квоту с помощью указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="5cb78-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="5cb78-133">Остановить-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="5cb78-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="5cb78-134">Отмена задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="5cb78-134">Cancel a managed disk migration job.</span></span>

