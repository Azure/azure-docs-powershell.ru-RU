---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732137"
---
# <span data-ttu-id="65a29-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="65a29-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="65a29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65a29-102">SYNOPSIS</span></span>
<span data-ttu-id="65a29-103">Проверка доступности имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="65a29-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65a29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65a29-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="65a29-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65a29-105">DESCRIPTION</span></span>
<span data-ttu-id="65a29-106">Командлет **Get-AzureRmStorageAccountNameAvailability** проверяет, является ли имя учетной записи службы хранилища Azure допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="65a29-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="65a29-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65a29-107">EXAMPLES</span></span>

### <span data-ttu-id="65a29-108">Пример 1: Проверка доступности имени учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="65a29-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="65a29-109">Эта команда проверяет доступность имени ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="65a29-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="65a29-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65a29-110">PARAMETERS</span></span>

### <span data-ttu-id="65a29-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="65a29-111">-Name</span></span>
<span data-ttu-id="65a29-112">Указывает имя учетной записи хранения, которую проверяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="65a29-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a29-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a29-113">CommonParameters</span></span>
<span data-ttu-id="65a29-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65a29-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a29-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a29-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a29-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65a29-116">INPUTS</span></span>

### <span data-ttu-id="65a29-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="65a29-117">None</span></span>
<span data-ttu-id="65a29-118">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="65a29-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="65a29-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65a29-119">OUTPUTS</span></span>

## <span data-ttu-id="65a29-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="65a29-120">NOTES</span></span>

## <span data-ttu-id="65a29-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65a29-121">RELATED LINKS</span></span>

[<span data-ttu-id="65a29-122">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="65a29-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)
