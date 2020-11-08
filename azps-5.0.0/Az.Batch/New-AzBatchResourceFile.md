---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248134"
---
# <span data-ttu-id="aa6f3-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="aa6f3-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="aa6f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6f3-103">Создание файла ресурсов для использования `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="aa6f3-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="aa6f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa6f3-104">SYNTAX</span></span>

### <span data-ttu-id="aa6f3-105">HttpUrl (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa6f3-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa6f3-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="aa6f3-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa6f3-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="aa6f3-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa6f3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa6f3-108">DESCRIPTION</span></span>
<span data-ttu-id="aa6f3-109">Создание файла ресурсов для использования `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="aa6f3-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="aa6f3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa6f3-110">EXAMPLES</span></span>

### <span data-ttu-id="aa6f3-111">Пример 1: создание файла ресурсов на основе URL-адреса HTTP, указывающего на один файл</span><span class="sxs-lookup"><span data-stu-id="aa6f3-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="aa6f3-112">Создает `PSResourceFile` ссылку на URL-адрес HTTP.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="aa6f3-113">Пример 2: создание файла ресурсов из URL-адреса контейнера хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="aa6f3-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="aa6f3-114">Создает `PSResourceFile` ссылку на URL-адрес контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="aa6f3-115">Все файлы в контейнере будут загружены в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="aa6f3-116">Пример 3: создание файла ресурсов из имени контейнера для автоматического хранения</span><span class="sxs-lookup"><span data-stu-id="aa6f3-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="aa6f3-117">Создает `PSResourceFile` ссылку на имя контейнера автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="aa6f3-118">Все файлы в контейнере будут загружены в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="aa6f3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa6f3-119">PARAMETERS</span></span>

### <span data-ttu-id="aa6f3-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="aa6f3-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="aa6f3-121">Имя контейнера хранилища в учетной записи автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="aa6f3-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="aa6f3-122">-BlobPrefix</span></span>
<span data-ttu-id="aa6f3-123">Получает префикс BLOB-объектов, который будет использоваться при загрузке больших двоичных объектов из контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="aa6f3-124">Будут загружены только те BLOB-объекты, имена которых начинаются с указанного префикса.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="aa6f3-125">Этот префикс может быть неполным именем файла или подкаталогом.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="aa6f3-126">Если префикс не указан, будут загружены все файлы в контейнере.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="aa6f3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa6f3-127">-DefaultProfile</span></span>
<span data-ttu-id="aa6f3-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa6f3-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="aa6f3-129">-FileMode</span></span>
<span data-ttu-id="aa6f3-130">Получает атрибут режима разрешений для файлов в восьмеричном формате.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="aa6f3-131">Это свойство применимо только в том случае, если файл ресурсов загружен на узел Linux.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="aa6f3-132">Если это свойство не задано для узла Linux, значение по умолчанию — 0770.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="aa6f3-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="aa6f3-133">-FilePath</span></span>
<span data-ttu-id="aa6f3-134">Расположение на вычислительном узле, в которое загружаются файлы, относящихся к рабочему каталогу задачи.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="aa6f3-135">Если указан параметр HttpUrl, необходимо указать путь к файлу и имя файла, в который будет загружен файл, включая его.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="aa6f3-136">В противном случае, если указаны параметры AutoStorageContainerName или StorageContainerUrl, путь является необязательным и является каталогом для загрузки файлов.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="aa6f3-137">В том случае, если путь FilePath используется в качестве каталога, все структуры каталогов, уже связанные с введенными данными, будут сохранены в полном виде и добавлены в указанный каталог FilePath.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="aa6f3-138">Указанный относительный путь не может прерывать рабочий каталог задачи (например, с помощью "...").</span><span class="sxs-lookup"><span data-stu-id="aa6f3-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="aa6f3-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="aa6f3-139">-HttpUrl</span></span>
<span data-ttu-id="aa6f3-140">URL-адрес файла, который нужно скачать.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-140">The URL of the file to download.</span></span>
<span data-ttu-id="aa6f3-141">Если URL — это хранилище BLOB-объектов Azure, оно должно быть доступно для чтения с помощью анонимного доступа; Это значит, что при загрузке большого двоичного объекта Служба пакетов не предоставляет никаких учетных данных.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="aa6f3-142">Существует два способа получения такого URL-адреса для большого двоичного объекта в хранилище Azure: Включите для него разрешения на чтение на доступ к большому двоичному объекту или установите для него ACL или контейнер, чтобы разрешить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="aa6f3-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="aa6f3-143">-StorageContainerUrl</span></span>
<span data-ttu-id="aa6f3-144">URL-адрес контейнера BLOB в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="aa6f3-145">Этот URL-адрес должен быть читаемым и доступен для просмотра с использованием анонимного доступа; Это значит, что при загрузке больших двоичных объектов из контейнера служба Batch не предоставляет никаких учетных данных.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="aa6f3-146">Существует два способа получения такого URL-адреса для контейнера в хранилище Azure: Включите на него подпись общего доступа (SAS), предоставляя разрешения на чтение для контейнера, или установите для контейнера ACL разрешение Public Access.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="aa6f3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6f3-147">CommonParameters</span></span>
<span data-ttu-id="aa6f3-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa6f3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6f3-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa6f3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6f3-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa6f3-150">INPUTS</span></span>

### <span data-ttu-id="aa6f3-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="aa6f3-151">None</span></span>

## <span data-ttu-id="aa6f3-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa6f3-152">OUTPUTS</span></span>

### <span data-ttu-id="aa6f3-153">Microsoft.Azure.Commands.BatCH. Models. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="aa6f3-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="aa6f3-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa6f3-154">NOTES</span></span>

## <span data-ttu-id="aa6f3-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa6f3-155">RELATED LINKS</span></span>

[<span data-ttu-id="aa6f3-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="aa6f3-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)