---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 578c32a27f53f586ec8a8013533e42928df48d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419956"
---
# <span data-ttu-id="66ad2-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="66ad2-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="66ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="66ad2-103">Начинается копирование исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="66ad2-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="66ad2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="66ad2-104">SYNTAX</span></span>

### <span data-ttu-id="66ad2-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="66ad2-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66ad2-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="66ad2-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="66ad2-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="66ad2-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="66ad2-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66ad2-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="66ad2-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="66ad2-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="66ad2-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="66ad2-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ad2-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="66ad2-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ad2-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66ad2-115">DESCRIPTION</span></span>
<span data-ttu-id="66ad2-116">Начинается **копирование** исходных файлов в исходный файл.</span><span class="sxs-lookup"><span data-stu-id="66ad2-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="66ad2-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="66ad2-117">EXAMPLES</span></span>

### <span data-ttu-id="66ad2-118">Пример 1. Запуск операции копирования из файла в файл с использованием имени и имени файла</span><span class="sxs-lookup"><span data-stu-id="66ad2-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="66ad2-119">Эта команда запускает операцию копирования из файла в файл.</span><span class="sxs-lookup"><span data-stu-id="66ad2-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="66ad2-120">Команда определяет имя и имя файла</span><span class="sxs-lookup"><span data-stu-id="66ad2-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="66ad2-121">Пример 2. Запуск операции копирования из BLOB-файлов в файл с использованием имени контейнера и имени BLOB-файла</span><span class="sxs-lookup"><span data-stu-id="66ad2-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="66ad2-122">Эта команда запускает операцию копирования из BLOB-файла в файл.</span><span class="sxs-lookup"><span data-stu-id="66ad2-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="66ad2-123">Команда определяет имя контейнера и имя BLOB-са.</span><span class="sxs-lookup"><span data-stu-id="66ad2-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="66ad2-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66ad2-124">PARAMETERS</span></span>

### <span data-ttu-id="66ad2-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="66ad2-125">-AbsoluteUri</span></span>
<span data-ttu-id="66ad2-126">Определяет URI для исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="66ad2-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="66ad2-127">Если для расположения источника требуются учетные данные, их необходимо предоставить.</span><span class="sxs-lookup"><span data-stu-id="66ad2-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="66ad2-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="66ad2-129">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="66ad2-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="66ad2-130">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="66ad2-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="66ad2-131">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="66ad2-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="66ad2-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="66ad2-133">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="66ad2-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="66ad2-134">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="66ad2-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="66ad2-135">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="66ad2-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="66ad2-136">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="66ad2-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="66ad2-137">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="66ad2-137">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-138">-Контекст</span><span class="sxs-lookup"><span data-stu-id="66ad2-138">-Context</span></span>
<span data-ttu-id="66ad2-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="66ad2-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="66ad2-140">Для получения контекста используйте New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="66ad2-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ad2-141">-DefaultProfile</span></span>
<span data-ttu-id="66ad2-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66ad2-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="66ad2-143">-DestContext</span></span>
<span data-ttu-id="66ad2-144">Определяет контекст хранилища Azure для назначения.</span><span class="sxs-lookup"><span data-stu-id="66ad2-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="66ad2-145">Чтобы получить контекст, используйте **New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="66ad2-145">To obtain a context, use **New-AzStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="66ad2-146">-DestFile</span></span>
<span data-ttu-id="66ad2-147">Указывает объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="66ad2-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="66ad2-148">Вы можете создать облачный файл или получить его с помощью Get-AzStorageFile-файла.</span><span class="sxs-lookup"><span data-stu-id="66ad2-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="66ad2-149">-DestFilePath</span></span>
<span data-ttu-id="66ad2-150">Путь к конечному файлу относительно конечной папки.</span><span class="sxs-lookup"><span data-stu-id="66ad2-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="66ad2-151">-DestShareName</span></span>
<span data-ttu-id="66ad2-152">Имя конечной вехи.</span><span class="sxs-lookup"><span data-stu-id="66ad2-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-153">-Force</span><span class="sxs-lookup"><span data-stu-id="66ad2-153">-Force</span></span>
<span data-ttu-id="66ad2-154">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="66ad2-154">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="66ad2-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="66ad2-156">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="66ad2-156">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="66ad2-157">-SrcBlob</span></span>
<span data-ttu-id="66ad2-158">Указывает объект **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="66ad2-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="66ad2-159">Вы можете создать облачный BLOB-проект или получить его с помощью Get-AzStorageBlob-управления.</span><span class="sxs-lookup"><span data-stu-id="66ad2-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="66ad2-160">-SrcBlobName</span></span>
<span data-ttu-id="66ad2-161">Имя источника BLOB-имени.</span><span class="sxs-lookup"><span data-stu-id="66ad2-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="66ad2-162">-SrcContainer</span></span>
<span data-ttu-id="66ad2-163">Указывает объект контейнера облачного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="66ad2-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="66ad2-164">Вы можете создать объект контейнера облачного BLOB-объекта или воспользоваться Get-AzStorageContainer-объектом.</span><span class="sxs-lookup"><span data-stu-id="66ad2-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="66ad2-165">-SrcContainerName</span></span>
<span data-ttu-id="66ad2-166">Имя контейнера-источника.</span><span class="sxs-lookup"><span data-stu-id="66ad2-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="66ad2-167">-SrcFile</span></span>
<span data-ttu-id="66ad2-168">Указывает объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="66ad2-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="66ad2-169">Вы можете создать облачный файл или получить его с помощью **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="66ad2-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="66ad2-170">-SrcFilePath</span></span>
<span data-ttu-id="66ad2-171">Путь к источнику файла относительно исходных каталогов или исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="66ad2-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="66ad2-172">-SrcShare</span></span>
<span data-ttu-id="66ad2-173">Указывает объект облачной папки.</span><span class="sxs-lookup"><span data-stu-id="66ad2-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="66ad2-174">Вы можете создать или получить облачную папку с помощью Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="66ad2-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="66ad2-175">-SrcShareName</span></span>
<span data-ttu-id="66ad2-176">Указывает имя источника.</span><span class="sxs-lookup"><span data-stu-id="66ad2-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66ad2-177">-Confirm</span></span>
<span data-ttu-id="66ad2-178">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66ad2-178">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ad2-179">-WhatIf</span></span>
<span data-ttu-id="66ad2-180">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66ad2-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ad2-181">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="66ad2-181">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ad2-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ad2-182">CommonParameters</span></span>
<span data-ttu-id="66ad2-183">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66ad2-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ad2-184">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ad2-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ad2-185">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66ad2-185">INPUTS</span></span>

### <span data-ttu-id="66ad2-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="66ad2-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="66ad2-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="66ad2-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="66ad2-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="66ad2-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66ad2-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="66ad2-189">OUTPUTS</span></span>

### <span data-ttu-id="66ad2-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="66ad2-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="66ad2-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="66ad2-191">NOTES</span></span>

## <span data-ttu-id="66ad2-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66ad2-192">RELATED LINKS</span></span>

[<span data-ttu-id="66ad2-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="66ad2-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="66ad2-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="66ad2-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="66ad2-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="66ad2-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="66ad2-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="66ad2-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="66ad2-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="66ad2-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="66ad2-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="66ad2-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
