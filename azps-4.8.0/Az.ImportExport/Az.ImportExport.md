---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242753"
---
# <span data-ttu-id="e4728-101">AZ. ImportExport Module</span><span class="sxs-lookup"><span data-stu-id="e4728-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="e4728-102">Nописание</span><span class="sxs-lookup"><span data-stu-id="e4728-102">Description</span></span>
<span data-ttu-id="e4728-103">Командлеты Microsoft Azure PowerShell: ImportExport</span><span class="sxs-lookup"><span data-stu-id="e4728-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="e4728-104">Командлеты AZ. ImportExport</span><span class="sxs-lookup"><span data-stu-id="e4728-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="e4728-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e4728-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="e4728-106">Получает сведения о существующем задании.</span><span class="sxs-lookup"><span data-stu-id="e4728-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="e4728-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="e4728-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="e4728-108">Возвращает ключи BitLocker для всех дисков в указанном задании.</span><span class="sxs-lookup"><span data-stu-id="e4728-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="e4728-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="e4728-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="e4728-110">Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="e4728-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="e4728-111">Расположение — это регион Azure.</span><span class="sxs-lookup"><span data-stu-id="e4728-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="e4728-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e4728-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="e4728-113">Создание нового задания или обновление существующего задания в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="e4728-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="e4728-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="e4728-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="e4728-115">Создайте объект DriverList для ImportExport.</span><span class="sxs-lookup"><span data-stu-id="e4728-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="e4728-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e4728-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="e4728-117">Удаление существующего задания.</span><span class="sxs-lookup"><span data-stu-id="e4728-117">Deletes an existing job.</span></span>
<span data-ttu-id="e4728-118">Удалять можно только задания в состоянии "создать" или "завершено".</span><span class="sxs-lookup"><span data-stu-id="e4728-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="e4728-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="e4728-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="e4728-120">Обновляет определенные свойства задания.</span><span class="sxs-lookup"><span data-stu-id="e4728-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="e4728-121">Вы можете вызвать эту операцию, чтобы уведомить службу импорта и экспорта о том, что жесткие диски, содержащие задания импорта или экспорта, отправлены в центр обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e4728-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="e4728-122">Она также может использоваться для отмены существующего задания.</span><span class="sxs-lookup"><span data-stu-id="e4728-122">It can also be used to cancel an existing job.</span></span>

