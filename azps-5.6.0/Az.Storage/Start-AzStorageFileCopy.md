---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 2b3bea343e5d4e2267c2bec14d60564392914a0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960072"
---
# <span data-ttu-id="4281c-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4281c-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="4281c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4281c-102">SYNOPSIS</span></span>
<span data-ttu-id="4281c-103">Начинается копирование исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="4281c-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="4281c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4281c-104">SYNTAX</span></span>

### <span data-ttu-id="4281c-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="4281c-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4281c-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4281c-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="4281c-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="4281c-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="4281c-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4281c-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="4281c-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="4281c-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="4281c-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="4281c-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4281c-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="4281c-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4281c-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4281c-115">DESCRIPTION</span></span>
<span data-ttu-id="4281c-116">Начинается **копирование** исходных файлов в исходный файл.</span><span class="sxs-lookup"><span data-stu-id="4281c-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="4281c-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4281c-117">EXAMPLES</span></span>

### <span data-ttu-id="4281c-118">Пример 1. Запуск операции копирования из файла в файл с использованием имени и имени файла</span><span class="sxs-lookup"><span data-stu-id="4281c-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="4281c-119">Эта команда запускает операцию копирования из файла в файл.</span><span class="sxs-lookup"><span data-stu-id="4281c-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="4281c-120">Команда определяет имя и имя файла</span><span class="sxs-lookup"><span data-stu-id="4281c-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="4281c-121">Пример 2. Запуск операции копирования из BLOB-файла в файл с использованием имени контейнера и имени BLOB-файла</span><span class="sxs-lookup"><span data-stu-id="4281c-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="4281c-122">Эта команда запускает операцию копирования из BLOB-файла в файл.</span><span class="sxs-lookup"><span data-stu-id="4281c-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="4281c-123">Команда определяет имя контейнера и имя BLOB-са.</span><span class="sxs-lookup"><span data-stu-id="4281c-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="4281c-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4281c-124">PARAMETERS</span></span>

### <span data-ttu-id="4281c-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="4281c-125">-AbsoluteUri</span></span>
<span data-ttu-id="4281c-126">Определяет URI для исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="4281c-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="4281c-127">Если для расположения источника требуются учетные данные, их необходимо предоставить.</span><span class="sxs-lookup"><span data-stu-id="4281c-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="4281c-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4281c-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4281c-129">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4281c-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4281c-130">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="4281c-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4281c-131">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4281c-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4281c-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4281c-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4281c-133">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="4281c-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4281c-134">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="4281c-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4281c-135">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="4281c-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4281c-136">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="4281c-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4281c-137">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4281c-137">The default value is 10.</span></span>

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

### <span data-ttu-id="4281c-138">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4281c-138">-Context</span></span>
<span data-ttu-id="4281c-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4281c-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4281c-140">Для получения контекста используйте New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4281c-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4281c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4281c-141">-DefaultProfile</span></span>
<span data-ttu-id="4281c-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4281c-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4281c-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="4281c-143">-DestContext</span></span>
<span data-ttu-id="4281c-144">Определяет контекст хранилища Azure для назначения.</span><span class="sxs-lookup"><span data-stu-id="4281c-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="4281c-145">Чтобы получить контекст, используйте **New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="4281c-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="4281c-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="4281c-146">-DestFile</span></span>
<span data-ttu-id="4281c-147">Указывает объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="4281c-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="4281c-148">Вы можете создать облачный файл или получить его с помощью Get-AzStorageFile-файла.</span><span class="sxs-lookup"><span data-stu-id="4281c-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="4281c-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="4281c-149">-DestFilePath</span></span>
<span data-ttu-id="4281c-150">Путь к конечному файлу относительно конечной папки.</span><span class="sxs-lookup"><span data-stu-id="4281c-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="4281c-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="4281c-151">-DestShareName</span></span>
<span data-ttu-id="4281c-152">Указывает имя конечной вехи.</span><span class="sxs-lookup"><span data-stu-id="4281c-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="4281c-153">-Force</span><span class="sxs-lookup"><span data-stu-id="4281c-153">-Force</span></span>
<span data-ttu-id="4281c-154">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4281c-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4281c-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4281c-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4281c-156">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="4281c-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4281c-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="4281c-157">-SrcBlob</span></span>
<span data-ttu-id="4281c-158">Указывает объект **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="4281c-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="4281c-159">Вы можете создать облачный большой проект или получить его с помощью Get-AzStorageBlob-управления.</span><span class="sxs-lookup"><span data-stu-id="4281c-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="4281c-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="4281c-160">-SrcBlobName</span></span>
<span data-ttu-id="4281c-161">Имя источника BLOB-имени.</span><span class="sxs-lookup"><span data-stu-id="4281c-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="4281c-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="4281c-162">-SrcContainer</span></span>
<span data-ttu-id="4281c-163">Указывает объект контейнера облачного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="4281c-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="4281c-164">Вы можете создать объект контейнера облачного BLOB-объекта или использовать Get-AzStorageContainer-проектлет.</span><span class="sxs-lookup"><span data-stu-id="4281c-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="4281c-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="4281c-165">-SrcContainerName</span></span>
<span data-ttu-id="4281c-166">Имя контейнера-источника.</span><span class="sxs-lookup"><span data-stu-id="4281c-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="4281c-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="4281c-167">-SrcFile</span></span>
<span data-ttu-id="4281c-168">Указывает объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="4281c-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="4281c-169">Вы можете создать облачный файл или получить его с помощью **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="4281c-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="4281c-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="4281c-170">-SrcFilePath</span></span>
<span data-ttu-id="4281c-171">Путь к источнику файла относительно исходных каталогов или исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="4281c-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="4281c-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="4281c-172">-SrcShare</span></span>
<span data-ttu-id="4281c-173">Указывает объект облачной папки.</span><span class="sxs-lookup"><span data-stu-id="4281c-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="4281c-174">Вы можете создать или получить облачную папку с помощью Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="4281c-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="4281c-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="4281c-175">-SrcShareName</span></span>
<span data-ttu-id="4281c-176">Указывает имя источника.</span><span class="sxs-lookup"><span data-stu-id="4281c-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="4281c-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4281c-177">-Confirm</span></span>
<span data-ttu-id="4281c-178">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4281c-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4281c-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4281c-179">-WhatIf</span></span>
<span data-ttu-id="4281c-180">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4281c-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4281c-181">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4281c-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4281c-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4281c-182">CommonParameters</span></span>
<span data-ttu-id="4281c-183">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4281c-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4281c-184">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4281c-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4281c-185">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4281c-185">INPUTS</span></span>

### <span data-ttu-id="4281c-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4281c-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="4281c-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="4281c-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="4281c-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4281c-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4281c-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4281c-189">OUTPUTS</span></span>

### <span data-ttu-id="4281c-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="4281c-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="4281c-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4281c-191">NOTES</span></span>

## <span data-ttu-id="4281c-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4281c-192">RELATED LINKS</span></span>

[<span data-ttu-id="4281c-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4281c-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="4281c-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4281c-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="4281c-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="4281c-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="4281c-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4281c-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4281c-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="4281c-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="4281c-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4281c-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
