---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 74088389-A003-4746-8A57-2146BBA7535C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0b86da15e81fd6eca005e04fc36b5887691af4bf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075851"
---
# <span data-ttu-id="090fa-101">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="090fa-101">Set-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="090fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="090fa-102">SYNOPSIS</span></span>
<span data-ttu-id="090fa-103">Обновление учетных данных для доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="090fa-103">Updates an Azure storage access credential.</span></span>

## <span data-ttu-id="090fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="090fa-104">SYNTAX</span></span>

```
Set-AzureStorSimpleStorageAccountCredential -StorageAccountName <String> [-StorageAccountKey <String>]
 [-UseSSL <Boolean>] [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="090fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="090fa-105">DESCRIPTION</span></span>
<span data-ttu-id="090fa-106">Командлет **Set-AzureStorSimpleStorageAccountCredential** Обновите существующие учетные данные доступа к хранилищу Azure для использования командлетами StorSimple OneSDK.</span><span class="sxs-lookup"><span data-stu-id="090fa-106">The **Set-AzureStorSimpleStorageAccountCredential** cmdlet update an existing Azure storage access credential for use by StorSimple OneSDK cmdlets.</span></span>
<span data-ttu-id="090fa-107">Дополнительные сведения о работе командлетов StorSimple с учетными записями хранения можно найти в разделе справки по командлету New-AzureStorSimpleStorageAccountCredential.</span><span class="sxs-lookup"><span data-stu-id="090fa-107">For more information about how StorSimple cmdlets work with storage accounts, see the help topic for the New-AzureStorSimpleStorageAccountCredential cmdlet.</span></span>

## <span data-ttu-id="090fa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="090fa-108">EXAMPLES</span></span>

### <span data-ttu-id="090fa-109">Пример 1: изменение учетных данных</span><span class="sxs-lookup"><span data-stu-id="090fa-109">Example 1: Modify a credential</span></span>
```
PS C:\>Set-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoStorage01" -UseSSL $False -StorageAccountKey "h9ldH4LlHJB3GujcNwgdxJACy1DaQ1Hak1bfoUBzrDqZ5DPK8+0XGbsgD+jrKfQy5PBepKpYobMViLaOC2XMdg==" -Force -WaitForComplete
VERBOSE: ClientRequestId: 20cd2b17-9cff-4ab4-a034-96d60d946295_PS
VERBOSE: ClientRequestId: a75ed193-1da5-491f-96f5-572b5461d466_PS
VERBOSE: ClientRequestId: db612c9e-e89a-404f-8406-e66e7f697cd5_PS
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: About to run a task to update your Storage Access credential! 
VERBOSE: ClientRequestId: a0995bb7-8223-4fcf-83c9-0a4f81e6a85c_PS


JobId        : 74a6172e-d47a-4824-a7fa-3eb207a76e0b
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: de04c77b-4846-45e0-9257-df501af9d4e9_PS
CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoStorage01
Name                             : ContosoStorage01
OperationInProgress              : None
Password                         : UUejow8u6ZynMm18g59883FBVtlIX6PWh6x+v15cnnkHKEAb5queTGnGOiGa/KkOqths7F/umDz+wUUB8zzq
                                   4YCi0Dm0rqPGDC4unhxvbncf+WeCEvV7qsf3pmUFdk8o96Cgl8oXgmmvYL9K6Z6ajHUdZFFlq9WqUpz2vBbz
                                   3ROxq8SRORt2DQVQP6LWojTiow1kNI/v2cs3eNvzoSgGftqzjSmhaTYu+q0o8X07eE4KwkWhQrRX24seH2Lg
                                   N9aYCQUrSxVKOAFJjdLOIBUlM48pnE7xyyZNwqngnPLt8z+mlS6JCKfo5SBKUfwmkhgDFfbVwB3jqC/sV/G6
                                   omwQ/A==
PasswordEncryptionCertThumbprint : 
UseSSL                           : False
VolumeCount                      : 0
```

<span data-ttu-id="090fa-110">Эта команда изменяет учетные данные учетной записи хранения с именем ContosoStorage01, чтобы больше не запрашивать SSL.</span><span class="sxs-lookup"><span data-stu-id="090fa-110">This command changes the storage account credential named ContosoStorage01 to no longer require SSL.</span></span>

## <span data-ttu-id="090fa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="090fa-111">PARAMETERS</span></span>

### <span data-ttu-id="090fa-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="090fa-112">-Profile</span></span>
<span data-ttu-id="090fa-113">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="090fa-113">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="090fa-114">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="090fa-114">-StorageAccountKey</span></span>
<span data-ttu-id="090fa-115">Задает клавишу доступа для учетной записи хранения в формате обычного текста.</span><span class="sxs-lookup"><span data-stu-id="090fa-115">Specifies the access key of the storage account in plain text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090fa-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="090fa-116">-StorageAccountName</span></span>
<span data-ttu-id="090fa-117">Указывает имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="090fa-117">Specifies the name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090fa-118">-UseSSL</span><span class="sxs-lookup"><span data-stu-id="090fa-118">-UseSSL</span></span>
<span data-ttu-id="090fa-119">Указывает, следует ли использовать SSL для подключения при использовании новых учетных данных учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="090fa-119">Indicates whether to use SSL for the connection when using the new storage account credential.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090fa-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="090fa-120">-WaitForComplete</span></span>
<span data-ttu-id="090fa-121">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="090fa-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="090fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="090fa-122">CommonParameters</span></span>
<span data-ttu-id="090fa-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="090fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="090fa-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="090fa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="090fa-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="090fa-125">INPUTS</span></span>

### <span data-ttu-id="090fa-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="090fa-126">None</span></span>

## <span data-ttu-id="090fa-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="090fa-127">OUTPUTS</span></span>

### <span data-ttu-id="090fa-128">StorageAccountCredentialResponse, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="090fa-128">StorageAccountCredentialResponse, TaskResponse</span></span>
<span data-ttu-id="090fa-129">Этот командлет возвращает объект **StorageAccountCredentialResponse** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="090fa-129">This cmdlet returns a **StorageAccountCredentialResponse** object, if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="090fa-130">Если этот параметр не указан, командлет возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="090fa-130">If you do not specify that parameter, the cmdlet returns a **TaskResponse** object.</span></span>
<span data-ttu-id="090fa-131">**StorageAccountCredentialResponse** имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="090fa-131">A **StorageAccountCredentialResponse** contains the following properties:</span></span> 

- <span data-ttu-id="090fa-132">**CloudType** ( **CloudType** )</span><span class="sxs-lookup"><span data-stu-id="090fa-132">**CloudType** ( **CloudType** )</span></span>
- <span data-ttu-id="090fa-133">**HostName** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-133">**Hostname** ( **String** )</span></span>
- <span data-ttu-id="090fa-134">**InstanceId** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-134">**InstanceId** ( **String** )</span></span>
- <span data-ttu-id="090fa-135">**По умолчанию** ( **Boolean** )</span><span class="sxs-lookup"><span data-stu-id="090fa-135">**IsDefault** ( **Boolean** )</span></span>
- <span data-ttu-id="090fa-136">**Расположение** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-136">**Location** ( **String** )</span></span>
- <span data-ttu-id="090fa-137">**Login** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-137">**Login** ( **String** )</span></span>
- <span data-ttu-id="090fa-138">**Name** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-138">**Name** ( **String** )</span></span>
- <span data-ttu-id="090fa-139">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="090fa-139">**OperationInProgress** ( **OperationInProgress** )</span></span>
- <span data-ttu-id="090fa-140">**Password** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-140">**Password** ( **String** )</span></span>
- <span data-ttu-id="090fa-141">**PasswordEncryptionCertThumbprint** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="090fa-141">**PasswordEncryptionCertThumbprint** ( **String** )</span></span>
- <span data-ttu-id="090fa-142">**UseSSL** ( **логическое значение** )</span><span class="sxs-lookup"><span data-stu-id="090fa-142">**UseSSL** ( **Boolean** )</span></span>
- <span data-ttu-id="090fa-143">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="090fa-143">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="090fa-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="090fa-144">NOTES</span></span>

## <span data-ttu-id="090fa-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="090fa-145">RELATED LINKS</span></span>

[<span data-ttu-id="090fa-146">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="090fa-146">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="090fa-147">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="090fa-147">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="090fa-148">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="090fa-148">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)


