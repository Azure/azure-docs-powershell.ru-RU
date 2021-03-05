---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: f8df4d49f0181b7cf8abf2581a522f953f3f2df7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007336"
---
# <span data-ttu-id="833ac-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="833ac-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="833ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="833ac-102">SYNOPSIS</span></span>
<span data-ttu-id="833ac-103">Создает файл ресурса для использования `New-AzBatchTask` по.</span><span class="sxs-lookup"><span data-stu-id="833ac-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="833ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="833ac-104">SYNTAX</span></span>

### <span data-ttu-id="833ac-105">HttpUrl (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="833ac-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="833ac-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="833ac-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="833ac-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="833ac-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="833ac-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="833ac-108">DESCRIPTION</span></span>
<span data-ttu-id="833ac-109">Создает файл ресурса для использования `New-AzBatchTask` по.</span><span class="sxs-lookup"><span data-stu-id="833ac-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="833ac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="833ac-110">EXAMPLES</span></span>

### <span data-ttu-id="833ac-111">Пример 1. Создание файла ресурса из URL-адреса HTTP, указываного на один файл</span><span class="sxs-lookup"><span data-stu-id="833ac-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="833ac-112">Создание `PSResourceFile` ССЫЛКи на HTTP-URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="833ac-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="833ac-113">Пример 2. Создание файла ресурса на url-адресе контейнера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="833ac-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="833ac-114">Создает URL-адрес контейнера хранилища `PSResourceFile` Azure.</span><span class="sxs-lookup"><span data-stu-id="833ac-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="833ac-115">Все файлы в контейнере будут загружены в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="833ac-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="833ac-116">Пример 3. Создание файла ресурса с именем контейнера автосъемки</span><span class="sxs-lookup"><span data-stu-id="833ac-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="833ac-117">Создание имени контейнера для `PSResourceFile` автосхранилища.</span><span class="sxs-lookup"><span data-stu-id="833ac-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="833ac-118">Все файлы в контейнере будут загружены в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="833ac-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="833ac-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="833ac-119">PARAMETERS</span></span>

### <span data-ttu-id="833ac-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="833ac-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="833ac-121">Имя контейнера хранилища в учетной записи автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="833ac-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="833ac-122">-BlobPrefix</span></span>
<span data-ttu-id="833ac-123">Возвращает префикс BLOB-lob, который будет использовать при скачии BLOB-людей из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="833ac-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="833ac-124">Будут скачины только те BLOB-lob, имена которых начинаются с указанного префикса.</span><span class="sxs-lookup"><span data-stu-id="833ac-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="833ac-125">Этот префикс может быть частью имени файла или поднаправлением.</span><span class="sxs-lookup"><span data-stu-id="833ac-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="833ac-126">Если префикс не указан, будут загружены все файлы в контейнере.</span><span class="sxs-lookup"><span data-stu-id="833ac-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="833ac-127">-DefaultProfile</span></span>
<span data-ttu-id="833ac-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="833ac-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="833ac-129">-FileMode</span></span>
<span data-ttu-id="833ac-130">Возвращает атрибут режима разрешений файла в восьмеся бытовом формате.</span><span class="sxs-lookup"><span data-stu-id="833ac-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="833ac-131">Это свойство применимо только в том случае, если файл ресурса загружается на узел Linux.</span><span class="sxs-lookup"><span data-stu-id="833ac-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="833ac-132">Если это свойство не задано для узла Linux, по умолчанию задано значение 0770.</span><span class="sxs-lookup"><span data-stu-id="833ac-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="833ac-133">-FilePath</span></span>
<span data-ttu-id="833ac-134">Расположение на узле вычислений, в которое нужно скачать файлы, относительно рабочего каталога задачи.</span><span class="sxs-lookup"><span data-stu-id="833ac-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="833ac-135">Если задан параметр HttpUrl, то параметр FilePath является required и описывает путь, в который нужно скачать файл, включая имя файла.</span><span class="sxs-lookup"><span data-stu-id="833ac-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="833ac-136">В противном случае, если заданы параметры AutoStorageContainerName или StorageContainerUrl, FilePath является необязательным и является каталогом, в который нужно скачать файлы.</span><span class="sxs-lookup"><span data-stu-id="833ac-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="833ac-137">В случае использования FilePath в качестве каталога любая структура каталога, уже связанная с входными данными, сохраняется полностью и ее можно будет ввести в указанный каталог FilePath.</span><span class="sxs-lookup"><span data-stu-id="833ac-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="833ac-138">Указанный относительный путь не может выйти из рабочего каталога задачи (например, с помощью ".").</span><span class="sxs-lookup"><span data-stu-id="833ac-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="833ac-139">-HttpUrl</span></span>
<span data-ttu-id="833ac-140">URL-адрес скачиваемого файла.</span><span class="sxs-lookup"><span data-stu-id="833ac-140">The URL of the file to download.</span></span>
<span data-ttu-id="833ac-141">Если URL-адресом является хранилище BLOB-хранилищ Azure, он должен быть прочитан с помощью анонимного доступа. то есть пакетная служба не может скачать BLOB-файл с учетными данными.</span><span class="sxs-lookup"><span data-stu-id="833ac-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="833ac-142">Получить такой URL-адрес для BLOB-сайта в хранилище Azure можно двумя способами: включить подпись общего доступа (SAS), которая предоставляет разрешения на чтение для этого двои такого хранилища, или настроить ACL для BLOB-сайта или его контейнера, чтобы разрешить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="833ac-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="833ac-143">-StorageContainerUrl</span></span>
<span data-ttu-id="833ac-144">URL-адрес контейнера BLOB-lob в хранилище BLOB-хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="833ac-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="833ac-145">Этот URL-адрес должен быть доступны для чтения и списка с использованием анонимного доступа; то есть пакетная служба не имеет учетных данных при скачии BLOB-людей из контейнера.</span><span class="sxs-lookup"><span data-stu-id="833ac-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="833ac-146">Получить такой URL-адрес для контейнера в хранилище Azure можно двумя способами: с использованием подписи SAS, которая предоставляет разрешения на чтение контейнера, или установить для него разрешение на общедоступный доступ.</span><span class="sxs-lookup"><span data-stu-id="833ac-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833ac-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833ac-147">CommonParameters</span></span>
<span data-ttu-id="833ac-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="833ac-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833ac-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="833ac-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833ac-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="833ac-150">INPUTS</span></span>

### <span data-ttu-id="833ac-151">Нет</span><span class="sxs-lookup"><span data-stu-id="833ac-151">None</span></span>

## <span data-ttu-id="833ac-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="833ac-152">OUTPUTS</span></span>

### <span data-ttu-id="833ac-153">Microsoft.Azure.Commands.Batch. Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="833ac-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="833ac-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="833ac-154">NOTES</span></span>

## <span data-ttu-id="833ac-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="833ac-155">RELATED LINKS</span></span>

[<span data-ttu-id="833ac-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="833ac-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)