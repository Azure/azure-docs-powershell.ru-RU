---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518693"
---
# <span data-ttu-id="d8c98-101">Модуль Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="d8c98-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="d8c98-102">Описание</span><span class="sxs-lookup"><span data-stu-id="d8c98-102">Description</span></span>
<span data-ttu-id="d8c98-103">Microsoft Azure PowerShell: импортэкспорта</span><span class="sxs-lookup"><span data-stu-id="d8c98-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="d8c98-104">Az.ImportExport Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d8c98-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="d8c98-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="d8c98-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="d8c98-106">Получает сведения о существующем задание.</span><span class="sxs-lookup"><span data-stu-id="d8c98-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="d8c98-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="d8c98-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="d8c98-108">Возвращает ключи BitLocker для всех дисков в указанном задание.</span><span class="sxs-lookup"><span data-stu-id="d8c98-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="d8c98-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="d8c98-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="d8c98-110">Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="d8c98-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="d8c98-111">Расположение — это регион Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c98-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="d8c98-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="d8c98-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="d8c98-113">Создание нового задания или обновление существующего задания в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="d8c98-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="d8c98-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="d8c98-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="d8c98-115">Создайте объект DriverList для ImportExport.</span><span class="sxs-lookup"><span data-stu-id="d8c98-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="d8c98-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="d8c98-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="d8c98-117">Удаляет существующее задание.</span><span class="sxs-lookup"><span data-stu-id="d8c98-117">Deletes an existing job.</span></span>
<span data-ttu-id="d8c98-118">Удалять можно только задания в состояниях создания и завершения.</span><span class="sxs-lookup"><span data-stu-id="d8c98-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="d8c98-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="d8c98-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="d8c98-120">Обновляет свойства задания.</span><span class="sxs-lookup"><span data-stu-id="d8c98-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="d8c98-121">Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, включающие задание импорта или экспорта, отправлены в центр обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d8c98-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="d8c98-122">Его также можно использовать для отмены существующего задания.</span><span class="sxs-lookup"><span data-stu-id="d8c98-122">It can also be used to cancel an existing job.</span></span>

