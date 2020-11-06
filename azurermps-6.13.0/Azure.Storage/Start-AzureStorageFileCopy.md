---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageFileCopy.md
ms.openlocfilehash: c5e071ddb5316f223260d3e6f239df4e75612332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565993"
---
# <span data-ttu-id="3ba2a-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3ba2a-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="3ba2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ba2a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba2a-103">Начинается копирование исходного файла.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ba2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ba2a-104">SYNTAX</span></span>

### <span data-ttu-id="3ba2a-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="3ba2a-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3ba2a-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="3ba2a-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="3ba2a-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-109">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="3ba2a-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="3ba2a-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="3ba2a-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="3ba2a-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="3ba2a-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ba2a-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="3ba2a-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ba2a-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba2a-115">DESCRIPTION</span></span>
<span data-ttu-id="3ba2a-116">Командлет **Start-AzureStorageFileCopy** запускает копирование исходного файла в конечный файл.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="3ba2a-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ba2a-117">EXAMPLES</span></span>

### <span data-ttu-id="3ba2a-118">Пример 1: запуск операции копирования из файла в файл с использованием имени общего доступа и имени файла</span><span class="sxs-lookup"><span data-stu-id="3ba2a-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="3ba2a-119">Эта команда запускает операцию копирования из файла в файл.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="3ba2a-120">Команда задает имя общего доступа и имя файла.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="3ba2a-121">Пример 2: запуск операции копирования из большого двоичного объекта в файл с использованием имени контейнера и имени BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="3ba2a-122">Эта команда запускает операцию копирования из BLOB-файла в файл.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="3ba2a-123">Команда задает имя контейнера и имя BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="3ba2a-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ba2a-124">PARAMETERS</span></span>

### <span data-ttu-id="3ba2a-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="3ba2a-125">-AbsoluteUri</span></span>
<span data-ttu-id="3ba2a-126">Задает универсальный код ресурса (URI) исходного файла.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="3ba2a-127">Если в исходном расположении требуются учетные данные, необходимо указать один из них.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="3ba2a-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ba2a-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3ba2a-129">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3ba2a-130">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3ba2a-131">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3ba2a-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3ba2a-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3ba2a-133">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3ba2a-134">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3ba2a-135">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3ba2a-136">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3ba2a-137">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-137">The default value is 10.</span></span>

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

### <span data-ttu-id="3ba2a-138">-Context</span><span class="sxs-lookup"><span data-stu-id="3ba2a-138">-Context</span></span>
<span data-ttu-id="3ba2a-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3ba2a-140">Чтобы получить контекст, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3ba2a-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba2a-141">-DefaultProfile</span></span>
<span data-ttu-id="3ba2a-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ba2a-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="3ba2a-143">-DestContext</span></span>
<span data-ttu-id="3ba2a-144">Указывает контекст хранилища Azure целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="3ba2a-145">Чтобы получить контекст, используйте **New-AzureStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

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

### <span data-ttu-id="3ba2a-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="3ba2a-146">-DestFile</span></span>
<span data-ttu-id="3ba2a-147">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="3ba2a-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3ba2a-148">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba2a-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="3ba2a-149">-DestFilePath</span></span>
<span data-ttu-id="3ba2a-150">Задает путь к файлу назначения относительно конечного общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="3ba2a-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="3ba2a-151">-DestShareName</span></span>
<span data-ttu-id="3ba2a-152">Указывает имя конечного общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="3ba2a-153">-Force</span><span class="sxs-lookup"><span data-stu-id="3ba2a-153">-Force</span></span>
<span data-ttu-id="3ba2a-154">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ba2a-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3ba2a-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3ba2a-156">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3ba2a-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="3ba2a-157">-SrcBlob</span></span>
<span data-ttu-id="3ba2a-158">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="3ba2a-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="3ba2a-159">Вы можете создать большой двоичный объект облака или получить его с помощью командлета Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba2a-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="3ba2a-160">-SrcBlobName</span></span>
<span data-ttu-id="3ba2a-161">Указывает имя исходного объекта BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="3ba2a-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="3ba2a-162">-SrcContainer</span></span>
<span data-ttu-id="3ba2a-163">Указывает объект контейнера BLOB-объектов в облаке.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="3ba2a-164">Вы можете создать объект контейнера BLOB-объектов облака или использовать командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba2a-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="3ba2a-165">-SrcContainerName</span></span>
<span data-ttu-id="3ba2a-166">Указывает имя исходного контейнера.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="3ba2a-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="3ba2a-167">-SrcFile</span></span>
<span data-ttu-id="3ba2a-168">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="3ba2a-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3ba2a-169">Вы можете создать файл в облаке или получить его с помощью **Get-AzureStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ba2a-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="3ba2a-170">-SrcFilePath</span></span>
<span data-ttu-id="3ba2a-171">Задает путь к исходному файлу относительно исходного каталога или исходной папки.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="3ba2a-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="3ba2a-172">-SrcShare</span></span>
<span data-ttu-id="3ba2a-173">Указывает облачный объект общего файлового типа.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="3ba2a-174">Вы можете создать облачную общую файловую систему или получить ее с помощью командлета Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ba2a-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="3ba2a-175">-SrcShareName</span></span>
<span data-ttu-id="3ba2a-176">Указывает имя исходного общего файла.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="3ba2a-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ba2a-177">-Confirm</span></span>
<span data-ttu-id="3ba2a-178">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ba2a-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ba2a-179">-WhatIf</span></span>
<span data-ttu-id="3ba2a-180">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ba2a-181">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ba2a-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba2a-182">CommonParameters</span></span>
<span data-ttu-id="3ba2a-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ba2a-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba2a-184">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ba2a-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba2a-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ba2a-185">INPUTS</span></span>

### <span data-ttu-id="3ba2a-186">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3ba2a-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3ba2a-187">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3ba2a-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="3ba2a-188">Параметры: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3ba2a-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="3ba2a-189">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3ba2a-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3ba2a-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ba2a-190">OUTPUTS</span></span>

### <span data-ttu-id="3ba2a-191">System. void</span><span class="sxs-lookup"><span data-stu-id="3ba2a-191">System.Void</span></span>

## <span data-ttu-id="3ba2a-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ba2a-192">NOTES</span></span>

## <span data-ttu-id="3ba2a-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ba2a-193">RELATED LINKS</span></span>

[<span data-ttu-id="3ba2a-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3ba2a-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="3ba2a-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3ba2a-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="3ba2a-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3ba2a-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3ba2a-197">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3ba2a-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="3ba2a-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="3ba2a-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="3ba2a-199">Остановить-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3ba2a-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
