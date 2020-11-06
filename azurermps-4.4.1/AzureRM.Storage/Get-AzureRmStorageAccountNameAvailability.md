---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8ca5c33944882fde7e9bad2411df5f41dbe5f788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563835"
---
# <span data-ttu-id="18dd0-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="18dd0-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="18dd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="18dd0-103">Проверка доступности имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="18dd0-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18dd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18dd0-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18dd0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="18dd0-106">Командлет **Get-AzureRmStorageAccountNameAvailability** проверяет, является ли имя учетной записи службы хранилища Azure допустимым и доступным для использования.</span><span class="sxs-lookup"><span data-stu-id="18dd0-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="18dd0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18dd0-107">EXAMPLES</span></span>

### <span data-ttu-id="18dd0-108">Пример 1: Проверка доступности имени учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="18dd0-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="18dd0-109">Эта команда проверяет доступность имени ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="18dd0-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="18dd0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18dd0-110">PARAMETERS</span></span>

### <span data-ttu-id="18dd0-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18dd0-111">-Name</span></span>
<span data-ttu-id="18dd0-112">Указывает имя учетной записи хранения, которую проверяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18dd0-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18dd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dd0-113">-DefaultProfile</span></span>
<span data-ttu-id="18dd0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18dd0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18dd0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dd0-115">CommonParameters</span></span>
<span data-ttu-id="18dd0-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18dd0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dd0-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18dd0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dd0-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18dd0-118">INPUTS</span></span>

## <span data-ttu-id="18dd0-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18dd0-119">OUTPUTS</span></span>

## <span data-ttu-id="18dd0-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="18dd0-120">NOTES</span></span>

## <span data-ttu-id="18dd0-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18dd0-121">RELATED LINKS</span></span>

[<span data-ttu-id="18dd0-122">Командлеты диспетчера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="18dd0-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


