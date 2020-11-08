---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 3c90e02194fa761bbb0fc00e11ea09d03ca00c1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080180"
---
# <span data-ttu-id="fcab7-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fcab7-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="fcab7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcab7-102">SYNOPSIS</span></span>
<span data-ttu-id="fcab7-103">Загружает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="fcab7-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="fcab7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcab7-104">SYNTAX</span></span>

### <span data-ttu-id="fcab7-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcab7-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="fcab7-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="fcab7-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="fcab7-107">Папка</span><span class="sxs-lookup"><span data-stu-id="fcab7-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="fcab7-108">Файл</span><span class="sxs-lookup"><span data-stu-id="fcab7-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="fcab7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcab7-109">DESCRIPTION</span></span>
<span data-ttu-id="fcab7-110">Командлет **Get-AzStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.</span><span class="sxs-lookup"><span data-stu-id="fcab7-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="fcab7-111">Этот командлет не возвращает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="fcab7-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="fcab7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcab7-112">EXAMPLES</span></span>

### <span data-ttu-id="fcab7-113">Пример 1: Загрузка файла из папки</span><span class="sxs-lookup"><span data-stu-id="fcab7-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="fcab7-114">Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="fcab7-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="fcab7-115">Пример 2: Загрузка файлов в разделе "пример общего файлового файла"</span><span class="sxs-lookup"><span data-stu-id="fcab7-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="fcab7-116">В этом примере загружаются файлы из примера общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="fcab7-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="fcab7-117">Пример 3: Скачайте файл Azure в локальный файл и perserve в файле Azure свойства SMB (файл Attributtes, время последнего создания файла, время последней записи) в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="fcab7-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="fcab7-118">В этом примере выполняется загрузка файла Azure в локальный файл и perserves в файле Azure свойства SMB (файл Attributtes, время создания файла, время последней записи) в локальном файле.</span><span class="sxs-lookup"><span data-stu-id="fcab7-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="fcab7-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcab7-119">PARAMETERS</span></span>

### <span data-ttu-id="fcab7-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcab7-120">-AsJob</span></span>
<span data-ttu-id="fcab7-121">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fcab7-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fcab7-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="fcab7-122">-CheckMd5</span></span>
<span data-ttu-id="fcab7-123">Указывает, следует ли проверять сумму Md5 для скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="fcab7-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="fcab7-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fcab7-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fcab7-125">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="fcab7-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="fcab7-126">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="fcab7-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="fcab7-127">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fcab7-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fcab7-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fcab7-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fcab7-129">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="fcab7-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="fcab7-130">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="fcab7-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="fcab7-131">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="fcab7-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="fcab7-132">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="fcab7-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="fcab7-133">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="fcab7-133">The default value is 10.</span></span>

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

### <span data-ttu-id="fcab7-134">-Context</span><span class="sxs-lookup"><span data-stu-id="fcab7-134">-Context</span></span>
<span data-ttu-id="fcab7-135">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab7-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="fcab7-136">Чтобы получить контекст, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fcab7-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fcab7-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcab7-137">-DefaultProfile</span></span>
<span data-ttu-id="fcab7-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab7-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcab7-139">-Destination</span><span class="sxs-lookup"><span data-stu-id="fcab7-139">-Destination</span></span>
<span data-ttu-id="fcab7-140">Указывает конечный путь.</span><span class="sxs-lookup"><span data-stu-id="fcab7-140">Specifies the destination path.</span></span>
<span data-ttu-id="fcab7-141">Этот командлет загружает содержимое файлов в расположение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fcab7-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="fcab7-142">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="fcab7-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fcab7-143">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="fcab7-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fcab7-144">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="fcab7-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="fcab7-145">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab7-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fcab7-146">-Каталог</span><span class="sxs-lookup"><span data-stu-id="fcab7-146">-Directory</span></span>
<span data-ttu-id="fcab7-147">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="fcab7-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="fcab7-148">Этот командлет получает содержимое файла в папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fcab7-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="fcab7-149">Чтобы получить каталог, используйте командлет New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="fcab7-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="fcab7-150">Вы также можете использовать командлет Get-AzStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="fcab7-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="fcab7-151">-Файл</span><span class="sxs-lookup"><span data-stu-id="fcab7-151">-File</span></span>
<span data-ttu-id="fcab7-152">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="fcab7-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="fcab7-153">Этот командлет получает файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fcab7-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="fcab7-154">Чтобы получить объект **CloudFile** , используйте командлет Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="fcab7-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="fcab7-155">-Force</span><span class="sxs-lookup"><span data-stu-id="fcab7-155">-Force</span></span>
<span data-ttu-id="fcab7-156">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="fcab7-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fcab7-157">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="fcab7-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fcab7-158">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="fcab7-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="fcab7-159">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fcab7-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fcab7-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcab7-160">-PassThru</span></span>
<span data-ttu-id="fcab7-161">Указывает на то, что этот командлет возвращает объект **AzureStorageFile** , который он загрузил.</span><span class="sxs-lookup"><span data-stu-id="fcab7-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="fcab7-162">-Path</span><span class="sxs-lookup"><span data-stu-id="fcab7-162">-Path</span></span>
<span data-ttu-id="fcab7-163">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="fcab7-163">Specifies the path of a file.</span></span>
<span data-ttu-id="fcab7-164">Этот командлет получает содержимое файла, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fcab7-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="fcab7-165">Если файл не существует, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fcab7-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fcab7-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="fcab7-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="fcab7-167">Сохранить в файле назначения свойства SMB исходного файла (файл Attributtes, время создания файла, время последней записи в файл).</span><span class="sxs-lookup"><span data-stu-id="fcab7-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="fcab7-168">Этот параметр доступен только в Windows.</span><span class="sxs-lookup"><span data-stu-id="fcab7-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="fcab7-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fcab7-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fcab7-170">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="fcab7-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="fcab7-171">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fcab7-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fcab7-172">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="fcab7-172">-Share</span></span>
<span data-ttu-id="fcab7-173">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="fcab7-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fcab7-174">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="fcab7-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="fcab7-175">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="fcab7-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="fcab7-176">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="fcab7-176">This object contains the storage context.</span></span>
<span data-ttu-id="fcab7-177">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="fcab7-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fcab7-178">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="fcab7-178">-ShareName</span></span>
<span data-ttu-id="fcab7-179">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="fcab7-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="fcab7-180">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="fcab7-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="fcab7-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcab7-181">-Confirm</span></span>
<span data-ttu-id="fcab7-182">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fcab7-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcab7-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcab7-183">-WhatIf</span></span>
<span data-ttu-id="fcab7-184">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fcab7-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcab7-185">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fcab7-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcab7-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcab7-186">CommonParameters</span></span>
<span data-ttu-id="fcab7-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcab7-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcab7-188">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcab7-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcab7-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcab7-189">INPUTS</span></span>

### <span data-ttu-id="fcab7-190">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fcab7-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="fcab7-191">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fcab7-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="fcab7-192">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="fcab7-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="fcab7-193">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fcab7-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fcab7-194">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcab7-194">OUTPUTS</span></span>

### <span data-ttu-id="fcab7-195">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fcab7-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="fcab7-196">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcab7-196">NOTES</span></span>

## <span data-ttu-id="fcab7-197">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcab7-197">RELATED LINKS</span></span>

[<span data-ttu-id="fcab7-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="fcab7-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="fcab7-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fcab7-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


