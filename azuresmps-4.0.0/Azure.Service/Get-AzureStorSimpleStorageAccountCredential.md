---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075551"
---
# <span data-ttu-id="8c5d3-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8c5d3-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="8c5d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5d3-103">Получает учетные данные для учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="8c5d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c5d3-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c5d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c5d3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c5d3-106">Командлет **Get-AzureStorSimpleStorageAccountCredential** получает учетные данные для учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="8c5d3-107">Этот командлет получает все объекты **StorageAccountCredential** , настроенные в службе или именованный **StorageAccountCredential**.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="8c5d3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c5d3-108">EXAMPLES</span></span>

### <span data-ttu-id="8c5d3-109">Пример 1: получение всех учетных данных для ресурса</span><span class="sxs-lookup"><span data-stu-id="8c5d3-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="8c5d3-110">Эта команда получает все доступные учетные данные для учетных записей хранения для текущего ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="8c5d3-111">Пример 2: получение учетных данных для определенной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8c5d3-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="8c5d3-112">Эта команда получает учетные данные учетной записи хранения для учетной записи хранения с именем ContosoCloudStorage.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="8c5d3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c5d3-113">PARAMETERS</span></span>

### <span data-ttu-id="8c5d3-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c5d3-114">-Profile</span></span>
<span data-ttu-id="8c5d3-115">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-115">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d3-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8c5d3-116">-StorageAccountName</span></span>
<span data-ttu-id="8c5d3-117">Указывает имя учетной записи хранения, для которой требуется получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5d3-118">CommonParameters</span></span>
<span data-ttu-id="8c5d3-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c5d3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5d3-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c5d3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5d3-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c5d3-121">INPUTS</span></span>

### <span data-ttu-id="8c5d3-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="8c5d3-122">None</span></span>

## <span data-ttu-id="8c5d3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c5d3-123">OUTPUTS</span></span>

### <span data-ttu-id="8c5d3-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="8c5d3-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="8c5d3-125">Этот командлет возвращает объект **StorageAccountCredential** , если указан параметр *StorageAccountName* , или, если этот параметр не указан, функция возвращает объект **IList \<StorageAccountCredential\>** .</span><span class="sxs-lookup"><span data-stu-id="8c5d3-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="8c5d3-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c5d3-126">NOTES</span></span>

## <span data-ttu-id="8c5d3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c5d3-127">RELATED LINKS</span></span>

[<span data-ttu-id="8c5d3-128">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8c5d3-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8c5d3-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8c5d3-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="8c5d3-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8c5d3-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)


