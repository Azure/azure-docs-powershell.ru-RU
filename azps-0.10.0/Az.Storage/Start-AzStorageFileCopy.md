---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 3336820514bbf4a949be2657d5955079efa87fac
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910645"
---
# <span data-ttu-id="6e34d-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6e34d-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="6e34d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e34d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e34d-103">Начинается копирование исходного файла.</span><span class="sxs-lookup"><span data-stu-id="6e34d-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="6e34d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e34d-104">SYNTAX</span></span>

### <span data-ttu-id="6e34d-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="6e34d-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e34d-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6e34d-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e34d-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="6e34d-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e34d-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="6e34d-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e34d-109">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="6e34d-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e34d-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="6e34d-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e34d-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="6e34d-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e34d-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="6e34d-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e34d-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="6e34d-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e34d-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="6e34d-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e34d-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e34d-115">DESCRIPTION</span></span>
<span data-ttu-id="6e34d-116">Командлет **Start-AzStorageFileCopy** запускает копирование исходного файла в конечный файл.</span><span class="sxs-lookup"><span data-stu-id="6e34d-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="6e34d-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e34d-117">EXAMPLES</span></span>

### <span data-ttu-id="6e34d-118">Пример 1: запуск операции копирования из файла в файл с использованием имени общего доступа и имени файла</span><span class="sxs-lookup"><span data-stu-id="6e34d-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="6e34d-119">Эта команда запускает операцию копирования из файла в файл.</span><span class="sxs-lookup"><span data-stu-id="6e34d-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="6e34d-120">Команда задает имя общего доступа и имя файла.</span><span class="sxs-lookup"><span data-stu-id="6e34d-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="6e34d-121">Пример 2: запуск операции копирования из большого двоичного объекта в файл с использованием имени контейнера и имени BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6e34d-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="6e34d-122">Эта команда запускает операцию копирования из BLOB-файла в файл.</span><span class="sxs-lookup"><span data-stu-id="6e34d-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="6e34d-123">Команда задает имя контейнера и имя BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6e34d-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="6e34d-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e34d-124">PARAMETERS</span></span>

### <span data-ttu-id="6e34d-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="6e34d-125">-AbsoluteUri</span></span>
<span data-ttu-id="6e34d-126">Задает универсальный код ресурса (URI) исходного файла.</span><span class="sxs-lookup"><span data-stu-id="6e34d-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="6e34d-127">Если в исходном расположении требуются учетные данные, необходимо указать один из них.</span><span class="sxs-lookup"><span data-stu-id="6e34d-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="6e34d-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e34d-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6e34d-129">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6e34d-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6e34d-130">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="6e34d-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6e34d-131">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e34d-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6e34d-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6e34d-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6e34d-133">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6e34d-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6e34d-134">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6e34d-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6e34d-135">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="6e34d-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6e34d-136">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="6e34d-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6e34d-137">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="6e34d-137">The default value is 10.</span></span>

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

### <span data-ttu-id="6e34d-138">-Context</span><span class="sxs-lookup"><span data-stu-id="6e34d-138">-Context</span></span>
<span data-ttu-id="6e34d-139">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6e34d-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6e34d-140">Чтобы получить контекст, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6e34d-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e34d-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e34d-141">-DefaultProfile</span></span>
<span data-ttu-id="6e34d-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e34d-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e34d-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="6e34d-143">-DestContext</span></span>
<span data-ttu-id="6e34d-144">Указывает контекст хранилища Azure целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6e34d-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="6e34d-145">Чтобы получить контекст, используйте **New-AzStorageContext**.</span><span class="sxs-lookup"><span data-stu-id="6e34d-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="6e34d-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="6e34d-146">-DestFile</span></span>
<span data-ttu-id="6e34d-147">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="6e34d-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="6e34d-148">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="6e34d-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="6e34d-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="6e34d-149">-DestFilePath</span></span>
<span data-ttu-id="6e34d-150">Задает путь к файлу назначения относительно конечного общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6e34d-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="6e34d-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="6e34d-151">-DestShareName</span></span>
<span data-ttu-id="6e34d-152">Указывает имя конечного общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6e34d-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="6e34d-153">-Force</span><span class="sxs-lookup"><span data-stu-id="6e34d-153">-Force</span></span>
<span data-ttu-id="6e34d-154">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6e34d-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e34d-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e34d-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6e34d-156">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="6e34d-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6e34d-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="6e34d-157">-SrcBlob</span></span>
<span data-ttu-id="6e34d-158">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="6e34d-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="6e34d-159">Вы можете создать большой двоичный объект облака или получить его с помощью командлета Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="6e34d-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6e34d-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="6e34d-160">-SrcBlobName</span></span>
<span data-ttu-id="6e34d-161">Указывает имя исходного объекта BLOB.</span><span class="sxs-lookup"><span data-stu-id="6e34d-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="6e34d-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="6e34d-162">-SrcContainer</span></span>
<span data-ttu-id="6e34d-163">Указывает объект контейнера BLOB-объектов в облаке.</span><span class="sxs-lookup"><span data-stu-id="6e34d-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="6e34d-164">Вы можете создать объект контейнера BLOB-объектов облака или использовать командлет Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="6e34d-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6e34d-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="6e34d-165">-SrcContainerName</span></span>
<span data-ttu-id="6e34d-166">Указывает имя исходного контейнера.</span><span class="sxs-lookup"><span data-stu-id="6e34d-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="6e34d-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="6e34d-167">-SrcFile</span></span>
<span data-ttu-id="6e34d-168">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="6e34d-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="6e34d-169">Вы можете создать файл в облаке или получить его с помощью **Get-AzStorageFile**.</span><span class="sxs-lookup"><span data-stu-id="6e34d-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

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

### <span data-ttu-id="6e34d-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="6e34d-170">-SrcFilePath</span></span>
<span data-ttu-id="6e34d-171">Задает путь к исходному файлу относительно исходного каталога или исходной папки.</span><span class="sxs-lookup"><span data-stu-id="6e34d-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="6e34d-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="6e34d-172">-SrcShare</span></span>
<span data-ttu-id="6e34d-173">Указывает облачный объект общего файлового типа.</span><span class="sxs-lookup"><span data-stu-id="6e34d-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="6e34d-174">Вы можете создать облачную общую файловую систему или получить ее с помощью командлета Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6e34d-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="6e34d-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="6e34d-175">-SrcShareName</span></span>
<span data-ttu-id="6e34d-176">Указывает имя исходного общего файла.</span><span class="sxs-lookup"><span data-stu-id="6e34d-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="6e34d-177">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e34d-177">-Confirm</span></span>
<span data-ttu-id="6e34d-178">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e34d-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e34d-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e34d-179">-WhatIf</span></span>
<span data-ttu-id="6e34d-180">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e34d-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e34d-181">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e34d-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e34d-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e34d-182">CommonParameters</span></span>
<span data-ttu-id="6e34d-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e34d-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e34d-184">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e34d-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e34d-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e34d-185">INPUTS</span></span>

### <span data-ttu-id="6e34d-186">Microsoft. WindowsAz. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6e34d-186">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6e34d-187">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="6e34d-187">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="6e34d-188">Параметры: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e34d-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="6e34d-189">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e34d-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e34d-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e34d-190">OUTPUTS</span></span>

### <span data-ttu-id="6e34d-191">System. void</span><span class="sxs-lookup"><span data-stu-id="6e34d-191">System.Void</span></span>

## <span data-ttu-id="6e34d-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e34d-192">NOTES</span></span>

## <span data-ttu-id="6e34d-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e34d-193">RELATED LINKS</span></span>

[<span data-ttu-id="6e34d-194">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6e34d-194">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6e34d-195">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6e34d-195">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="6e34d-196">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="6e34d-196">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="6e34d-197">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="6e34d-197">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="6e34d-198">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="6e34d-198">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="6e34d-199">Остановить-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6e34d-199">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
