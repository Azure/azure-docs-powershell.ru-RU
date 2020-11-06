---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: ''
schema: 2.0.0
ms.openlocfilehash: c945838d7d237fb37610d3763525b0ecac838fbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556260"
---
# <span data-ttu-id="30e60-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30e60-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="30e60-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30e60-102">SYNOPSIS</span></span>
<span data-ttu-id="30e60-103">Загружает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="30e60-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="30e60-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30e60-104">SYNTAX</span></span>

### <span data-ttu-id="30e60-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30e60-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30e60-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="30e60-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30e60-107">Папка</span><span class="sxs-lookup"><span data-stu-id="30e60-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30e60-108">Файл</span><span class="sxs-lookup"><span data-stu-id="30e60-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30e60-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30e60-109">DESCRIPTION</span></span>
<span data-ttu-id="30e60-110">Командлет **Get-AzureStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.</span><span class="sxs-lookup"><span data-stu-id="30e60-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="30e60-111">Этот командлет не возвращает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="30e60-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="30e60-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30e60-112">EXAMPLES</span></span>

### <span data-ttu-id="30e60-113">Пример 1: Загрузка файла из папки</span><span class="sxs-lookup"><span data-stu-id="30e60-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="30e60-114">Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="30e60-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

## <span data-ttu-id="30e60-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30e60-115">PARAMETERS</span></span>

### <span data-ttu-id="30e60-116">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="30e60-116">-CheckMd5</span></span>
<span data-ttu-id="30e60-117">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-117">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-118">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-118">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-119">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-119">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-120">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-120">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30e60-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="30e60-122">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-122">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-123">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-123">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-124">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-124">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-125">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-125">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="30e60-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="30e60-127">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-127">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-128">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-128">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-129">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-129">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-130">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-130">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-131">-Context</span><span class="sxs-lookup"><span data-stu-id="30e60-131">-Context</span></span>
<span data-ttu-id="30e60-132">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-132">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-133">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-133">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-134">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-134">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-135">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-135">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-136">-Destination</span><span class="sxs-lookup"><span data-stu-id="30e60-136">-Destination</span></span>
<span data-ttu-id="30e60-137">Указывает конечный путь.</span><span class="sxs-lookup"><span data-stu-id="30e60-137">Specifies the destination path.</span></span>
<span data-ttu-id="30e60-138">Этот командлет загружает содержимое файлов в расположение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="30e60-138">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="30e60-139">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-139">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-140">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-140">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-141">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-141">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-142">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-142">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-143">-Каталог</span><span class="sxs-lookup"><span data-stu-id="30e60-143">-Directory</span></span>
<span data-ttu-id="30e60-144">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="30e60-144">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="30e60-145">Этот командлет получает содержимое файла в папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="30e60-145">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="30e60-146">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="30e60-146">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="30e60-147">Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="30e60-147">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="30e60-148">-Файл</span><span class="sxs-lookup"><span data-stu-id="30e60-148">-File</span></span>
<span data-ttu-id="30e60-149">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="30e60-149">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="30e60-150">Этот командлет получает файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="30e60-150">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="30e60-151">Чтобы получить объект **CloudFile** , используйте командлет Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="30e60-151">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="30e60-152">-Force</span><span class="sxs-lookup"><span data-stu-id="30e60-152">-Force</span></span>
<span data-ttu-id="30e60-153">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-153">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-154">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-154">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-155">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-155">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-156">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-156">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-157">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30e60-157">-PassThru</span></span>
<span data-ttu-id="30e60-158">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-158">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-159">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-159">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-160">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-160">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-161">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-161">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-162">-Path</span><span class="sxs-lookup"><span data-stu-id="30e60-162">-Path</span></span>
<span data-ttu-id="30e60-163">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="30e60-163">Specifies the path of a file.</span></span>
<span data-ttu-id="30e60-164">Этот командлет получает содержимое файла, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="30e60-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="30e60-165">Если файл не существует, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="30e60-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="30e60-166">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30e60-166">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="30e60-167">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="30e60-167">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="30e60-168">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="30e60-168">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="30e60-169">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="30e60-169">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="30e60-170">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="30e60-170">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="30e60-171">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="30e60-171">-Share</span></span>
<span data-ttu-id="30e60-172">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="30e60-172">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="30e60-173">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="30e60-173">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="30e60-174">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="30e60-174">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="30e60-175">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="30e60-175">This object contains the storage context.</span></span>
<span data-ttu-id="30e60-176">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="30e60-176">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="30e60-177">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="30e60-177">-ShareName</span></span>
<span data-ttu-id="30e60-178">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="30e60-178">Specifies the name of the file share.</span></span>
<span data-ttu-id="30e60-179">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="30e60-179">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="30e60-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30e60-180">-Confirm</span></span>
<span data-ttu-id="30e60-181">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30e60-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e60-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e60-182">-WhatIf</span></span>
<span data-ttu-id="30e60-183">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30e60-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30e60-184">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30e60-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e60-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e60-185">CommonParameters</span></span>
<span data-ttu-id="30e60-186">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30e60-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e60-187">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e60-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e60-188">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30e60-188">INPUTS</span></span>

## <span data-ttu-id="30e60-189">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30e60-189">OUTPUTS</span></span>

## <span data-ttu-id="30e60-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="30e60-190">NOTES</span></span>

## <span data-ttu-id="30e60-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30e60-191">RELATED LINKS</span></span>

[<span data-ttu-id="30e60-192">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="30e60-192">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="30e60-193">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30e60-193">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


