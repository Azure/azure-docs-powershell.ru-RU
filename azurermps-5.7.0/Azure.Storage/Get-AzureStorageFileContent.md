---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565092"
---
# <span data-ttu-id="3c401-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3c401-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="3c401-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c401-102">SYNOPSIS</span></span>
<span data-ttu-id="3c401-103">Загружает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="3c401-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c401-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c401-104">SYNTAX</span></span>

### <span data-ttu-id="3c401-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c401-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c401-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="3c401-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c401-107">Папка</span><span class="sxs-lookup"><span data-stu-id="3c401-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c401-108">Файл</span><span class="sxs-lookup"><span data-stu-id="3c401-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c401-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c401-109">DESCRIPTION</span></span>
<span data-ttu-id="3c401-110">Командлет **Get-AzureStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.</span><span class="sxs-lookup"><span data-stu-id="3c401-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="3c401-111">Этот командлет не возвращает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="3c401-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="3c401-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c401-112">EXAMPLES</span></span>

### <span data-ttu-id="3c401-113">Пример 1: Загрузка файла из папки</span><span class="sxs-lookup"><span data-stu-id="3c401-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="3c401-114">Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="3c401-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="3c401-115">Пример 2: Загрузка файлов в разделе "пример общего файлового файла"</span><span class="sxs-lookup"><span data-stu-id="3c401-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="3c401-116">В этом примере загружаются файлы из примера общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="3c401-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="3c401-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c401-117">PARAMETERS</span></span>

### <span data-ttu-id="3c401-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="3c401-118">-CheckMd5</span></span>
<span data-ttu-id="3c401-119">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-120">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-121">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-122">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3c401-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3c401-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3c401-124">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-125">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-126">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-127">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3c401-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3c401-129">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-130">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-131">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-132">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-133">-Context</span><span class="sxs-lookup"><span data-stu-id="3c401-133">-Context</span></span>
<span data-ttu-id="3c401-134">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-135">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-136">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-137">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-138">-Destination</span><span class="sxs-lookup"><span data-stu-id="3c401-138">-Destination</span></span>
<span data-ttu-id="3c401-139">Указывает конечный путь.</span><span class="sxs-lookup"><span data-stu-id="3c401-139">Specifies the destination path.</span></span>
<span data-ttu-id="3c401-140">Этот командлет загружает содержимое файлов в расположение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3c401-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="3c401-141">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-142">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-143">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-144">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-145">-Каталог</span><span class="sxs-lookup"><span data-stu-id="3c401-145">-Directory</span></span>
<span data-ttu-id="3c401-146">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="3c401-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3c401-147">Этот командлет получает содержимое файла в папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3c401-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="3c401-148">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="3c401-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3c401-149">Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="3c401-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-150">-Файл</span><span class="sxs-lookup"><span data-stu-id="3c401-150">-File</span></span>
<span data-ttu-id="3c401-151">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="3c401-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="3c401-152">Этот командлет получает файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3c401-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="3c401-153">Чтобы получить объект **CloudFile** , используйте командлет Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="3c401-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-154">-Force</span><span class="sxs-lookup"><span data-stu-id="3c401-154">-Force</span></span>
<span data-ttu-id="3c401-155">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-156">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-157">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-158">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3c401-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c401-159">-PassThru</span></span>
<span data-ttu-id="3c401-160">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-161">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-162">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-163">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="3c401-164">-Path</span><span class="sxs-lookup"><span data-stu-id="3c401-164">-Path</span></span>
<span data-ttu-id="3c401-165">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="3c401-165">Specifies the path of a file.</span></span>
<span data-ttu-id="3c401-166">Этот командлет получает содержимое файла, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3c401-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="3c401-167">Если файл не существует, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3c401-167">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3c401-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3c401-169">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="3c401-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="3c401-170">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="3c401-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="3c401-171">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="3c401-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="3c401-172">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3c401-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-173">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="3c401-173">-Share</span></span>
<span data-ttu-id="3c401-174">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="3c401-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3c401-175">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="3c401-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="3c401-176">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="3c401-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="3c401-177">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="3c401-177">This object contains the storage context.</span></span>
<span data-ttu-id="3c401-178">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="3c401-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-179">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="3c401-179">-ShareName</span></span>
<span data-ttu-id="3c401-180">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="3c401-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="3c401-181">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="3c401-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c401-182">-Confirm</span></span>
<span data-ttu-id="3c401-183">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c401-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c401-184">-WhatIf</span></span>
<span data-ttu-id="3c401-185">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c401-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c401-186">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c401-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c401-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c401-187">CommonParameters</span></span>
<span data-ttu-id="3c401-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c401-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c401-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c401-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c401-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c401-190">INPUTS</span></span>

### <span data-ttu-id="3c401-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c401-191">IStorageContext</span></span>

<span data-ttu-id="3c401-192">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c401-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3c401-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3c401-193">CloudFileDirectory</span></span>

<span data-ttu-id="3c401-194">Параметр "Directory" принимает значение типа "CloudFileDirectory" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c401-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="3c401-195">CloudFile</span><span class="sxs-lookup"><span data-stu-id="3c401-195">CloudFile</span></span>

<span data-ttu-id="3c401-196">Параметр "файл" принимает значение типа "CloudFile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c401-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="3c401-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3c401-197">CloudFileShare</span></span>

<span data-ttu-id="3c401-198">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c401-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="3c401-199">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c401-199">OUTPUTS</span></span>

## <span data-ttu-id="3c401-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c401-200">NOTES</span></span>

## <span data-ttu-id="3c401-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c401-201">RELATED LINKS</span></span>

[<span data-ttu-id="3c401-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3c401-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3c401-203">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3c401-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


