---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 33fcfabb50b0b4af73fe7111c587ac88e746598e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981512"
---
# <span data-ttu-id="e954e-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e954e-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="e954e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e954e-102">SYNOPSIS</span></span>
<span data-ttu-id="e954e-103">Скачивает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="e954e-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="e954e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e954e-104">SYNTAX</span></span>

### <span data-ttu-id="e954e-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e954e-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="e954e-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="e954e-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="e954e-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="e954e-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="e954e-108">Файл</span><span class="sxs-lookup"><span data-stu-id="e954e-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="e954e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e954e-109">DESCRIPTION</span></span>
<span data-ttu-id="e954e-110">**Cmdlet Get-AzStorageFileContent** скачивает содержимое файла и сохраняет его в задаваемом месте.</span><span class="sxs-lookup"><span data-stu-id="e954e-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="e954e-111">Этот cmdlet не возвращает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="e954e-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="e954e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e954e-112">EXAMPLES</span></span>

### <span data-ttu-id="e954e-113">Пример 1. Скачивание файла из папки</span><span class="sxs-lookup"><span data-stu-id="e954e-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="e954e-114">Эта команда скачивает файл с именем CurrentDataFile из папки ContosoWorkingFolder из папки ContosoShare06 в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="e954e-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="e954e-115">Пример 2. Скачивает файлы из примера папки</span><span class="sxs-lookup"><span data-stu-id="e954e-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="e954e-116">В этом примере файлы загружаются в образце файловой папки</span><span class="sxs-lookup"><span data-stu-id="e954e-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="e954e-117">Пример 3. Скачайте файл Azure в локальный файл и заблокируете свойства SMB-файлов Azure ("Файл привяжите", "Время создания файла", "Время последней записи") в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="e954e-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="e954e-118">В этом примере файл Azure скачивается в локальный файл, а свойства SMB-файла Azure ("Файл авторт", "Время создания файла", "Время последней записи файла") будут в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="e954e-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="e954e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e954e-119">PARAMETERS</span></span>

### <span data-ttu-id="e954e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e954e-120">-AsJob</span></span>
<span data-ttu-id="e954e-121">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="e954e-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e954e-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="e954e-122">-CheckMd5</span></span>
<span data-ttu-id="e954e-123">Указывает, нужно ли проверять сумму Md5 для загруженного файла.</span><span class="sxs-lookup"><span data-stu-id="e954e-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="e954e-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e954e-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e954e-125">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e954e-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="e954e-126">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="e954e-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="e954e-127">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e954e-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e954e-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e954e-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e954e-129">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="e954e-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="e954e-130">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="e954e-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="e954e-131">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="e954e-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="e954e-132">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="e954e-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="e954e-133">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e954e-133">The default value is 10.</span></span>

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

### <span data-ttu-id="e954e-134">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e954e-134">-Context</span></span>
<span data-ttu-id="e954e-135">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e954e-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="e954e-136">Для получения контекста используйте New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e954e-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e954e-137">-DefaultProfile</span></span>
<span data-ttu-id="e954e-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e954e-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e954e-139">-Destination</span><span class="sxs-lookup"><span data-stu-id="e954e-139">-Destination</span></span>
<span data-ttu-id="e954e-140">Путь назначения.</span><span class="sxs-lookup"><span data-stu-id="e954e-140">Specifies the destination path.</span></span>
<span data-ttu-id="e954e-141">Этот cmdlet скачивает содержимое файла в расположение, указанное этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e954e-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="e954e-142">Если указать путь к не существует файлу, этот cmdlet создаст этот файл и сохранит его содержимое.</span><span class="sxs-lookup"><span data-stu-id="e954e-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e954e-143">Если указать путь к файлу, который уже существует, и задать параметр *Force,* этот cmdlet переопишет файл.</span><span class="sxs-lookup"><span data-stu-id="e954e-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e954e-144">Если вы указали путь к существующему файлу, но не укакнули "Принудительно", то перед тем как продолжать, будет предложено сделать это.</span><span class="sxs-lookup"><span data-stu-id="e954e-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e954e-145">Если указать путь к папке, этот cmdlet пытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e954e-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-146">-Каталог</span><span class="sxs-lookup"><span data-stu-id="e954e-146">-Directory</span></span>
<span data-ttu-id="e954e-147">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="e954e-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="e954e-148">Этот cmdlet получает содержимое файла в папке, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e954e-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="e954e-149">Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="e954e-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="e954e-150">Для получения каталога Get-AzStorageFile можно также воспользоваться этим Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="e954e-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-151">-File</span><span class="sxs-lookup"><span data-stu-id="e954e-151">-File</span></span>
<span data-ttu-id="e954e-152">Определяет файл как объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="e954e-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="e954e-153">Этот cmdlet возвращает файл, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e954e-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="e954e-154">Чтобы получить объект **CloudFile,** воспользуйтесь Get-AzStorageFile управления.</span><span class="sxs-lookup"><span data-stu-id="e954e-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-155">-Force</span><span class="sxs-lookup"><span data-stu-id="e954e-155">-Force</span></span>
<span data-ttu-id="e954e-156">Если указать путь к не существует файлу, этот cmdlet создаст этот файл и сохранит его содержимое.</span><span class="sxs-lookup"><span data-stu-id="e954e-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="e954e-157">Если указать путь к файлу, который уже существует, и задать параметр *Force,* этот cmdlet переопишет файл.</span><span class="sxs-lookup"><span data-stu-id="e954e-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="e954e-158">Если вы указали путь к существующему файлу, но не укакнули "Принудительно", то перед тем как продолжать, будет предложено сделать это.</span><span class="sxs-lookup"><span data-stu-id="e954e-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="e954e-159">Если указать путь к папке, этот cmdlet пытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e954e-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="e954e-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e954e-160">-PassThru</span></span>
<span data-ttu-id="e954e-161">Указывает на то, что этот cmdlet возвращает объект **AzureStorageFile,** который он скачивает.</span><span class="sxs-lookup"><span data-stu-id="e954e-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="e954e-162">-Path</span><span class="sxs-lookup"><span data-stu-id="e954e-162">-Path</span></span>
<span data-ttu-id="e954e-163">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="e954e-163">Specifies the path of a file.</span></span>
<span data-ttu-id="e954e-164">Этот cmdlet возвращает содержимое файла, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e954e-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="e954e-165">Если файл не существует, этот cmdlet возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e954e-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="e954e-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="e954e-167">Сохранить исходные свойства SMB-файла (File Attributtes, время создания файла, время последней записи файла) в нужном файле.</span><span class="sxs-lookup"><span data-stu-id="e954e-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="e954e-168">Этот параметр доступен только в Windows.</span><span class="sxs-lookup"><span data-stu-id="e954e-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="e954e-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e954e-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e954e-170">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="e954e-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="e954e-171">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e954e-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="e954e-172">-Share</span><span class="sxs-lookup"><span data-stu-id="e954e-172">-Share</span></span>
<span data-ttu-id="e954e-173">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="e954e-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e954e-174">Этот cmdlet downloads the contents of the file in the share this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="e954e-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="e954e-175">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="e954e-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="e954e-176">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="e954e-176">This object contains the storage context.</span></span>
<span data-ttu-id="e954e-177">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="e954e-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e954e-178">-ShareName</span></span>
<span data-ttu-id="e954e-179">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="e954e-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="e954e-180">Этот cmdlet downloads the contents of the file in the share this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="e954e-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e954e-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e954e-181">-Confirm</span></span>
<span data-ttu-id="e954e-182">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e954e-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e954e-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e954e-183">-WhatIf</span></span>
<span data-ttu-id="e954e-184">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e954e-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e954e-185">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e954e-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e954e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e954e-186">CommonParameters</span></span>
<span data-ttu-id="e954e-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e954e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e954e-188">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e954e-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e954e-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e954e-189">INPUTS</span></span>

### <span data-ttu-id="e954e-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e954e-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e954e-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="e954e-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="e954e-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="e954e-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="e954e-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e954e-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e954e-194">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e954e-194">OUTPUTS</span></span>

### <span data-ttu-id="e954e-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e954e-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="e954e-196">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e954e-196">NOTES</span></span>

## <span data-ttu-id="e954e-197">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e954e-197">RELATED LINKS</span></span>

[<span data-ttu-id="e954e-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e954e-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="e954e-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e954e-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


