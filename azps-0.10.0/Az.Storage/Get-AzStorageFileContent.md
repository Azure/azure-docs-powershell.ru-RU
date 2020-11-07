---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910767"
---
# <span data-ttu-id="7fe71-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fe71-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="7fe71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fe71-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe71-103">Загружает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="7fe71-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="7fe71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fe71-104">SYNTAX</span></span>

### <span data-ttu-id="7fe71-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fe71-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fe71-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="7fe71-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fe71-107">Папка</span><span class="sxs-lookup"><span data-stu-id="7fe71-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fe71-108">Файл</span><span class="sxs-lookup"><span data-stu-id="7fe71-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fe71-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fe71-109">DESCRIPTION</span></span>
<span data-ttu-id="7fe71-110">Командлет **Get-AzStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.</span><span class="sxs-lookup"><span data-stu-id="7fe71-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="7fe71-111">Этот командлет не возвращает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="7fe71-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="7fe71-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fe71-112">EXAMPLES</span></span>

### <span data-ttu-id="7fe71-113">Пример 1: Загрузка файла из папки</span><span class="sxs-lookup"><span data-stu-id="7fe71-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="7fe71-114">Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="7fe71-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="7fe71-115">Пример 2: Загрузка файлов в разделе "пример общего файлового файла"</span><span class="sxs-lookup"><span data-stu-id="7fe71-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="7fe71-116">В этом примере загружаются файлы из примера общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="7fe71-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="7fe71-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fe71-117">PARAMETERS</span></span>

### <span data-ttu-id="7fe71-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="7fe71-118">-CheckMd5</span></span>
<span data-ttu-id="7fe71-119">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-120">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-121">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-122">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7fe71-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7fe71-124">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-125">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-126">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-127">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7fe71-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7fe71-129">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-130">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-131">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-132">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-133">-Context</span><span class="sxs-lookup"><span data-stu-id="7fe71-133">-Context</span></span>
<span data-ttu-id="7fe71-134">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-135">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-136">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-137">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe71-138">-DefaultProfile</span></span>
<span data-ttu-id="7fe71-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fe71-140">-Destination</span><span class="sxs-lookup"><span data-stu-id="7fe71-140">-Destination</span></span>
<span data-ttu-id="7fe71-141">Указывает конечный путь.</span><span class="sxs-lookup"><span data-stu-id="7fe71-141">Specifies the destination path.</span></span>
<span data-ttu-id="7fe71-142">Этот командлет загружает содержимое файлов в расположение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7fe71-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="7fe71-143">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-144">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-145">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-146">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-147">-Каталог</span><span class="sxs-lookup"><span data-stu-id="7fe71-147">-Directory</span></span>
<span data-ttu-id="7fe71-148">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="7fe71-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="7fe71-149">Этот командлет получает содержимое файла в папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7fe71-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="7fe71-150">Чтобы получить каталог, используйте командлет New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="7fe71-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="7fe71-151">Вы также можете использовать командлет Get-AzStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="7fe71-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe71-152">-Файл</span><span class="sxs-lookup"><span data-stu-id="7fe71-152">-File</span></span>
<span data-ttu-id="7fe71-153">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="7fe71-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="7fe71-154">Этот командлет получает файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7fe71-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="7fe71-155">Чтобы получить объект **CloudFile** , используйте командлет Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="7fe71-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe71-156">-Force</span><span class="sxs-lookup"><span data-stu-id="7fe71-156">-Force</span></span>
<span data-ttu-id="7fe71-157">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-158">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-159">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-160">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fe71-161">-PassThru</span></span>
<span data-ttu-id="7fe71-162">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-163">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-164">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-165">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-166">-Path</span><span class="sxs-lookup"><span data-stu-id="7fe71-166">-Path</span></span>
<span data-ttu-id="7fe71-167">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="7fe71-167">Specifies the path of a file.</span></span>
<span data-ttu-id="7fe71-168">Этот командлет получает содержимое файла, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7fe71-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="7fe71-169">Если файл не существует, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7fe71-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7fe71-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7fe71-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7fe71-171">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="7fe71-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="7fe71-172">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="7fe71-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="7fe71-173">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="7fe71-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="7fe71-174">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe71-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="7fe71-175">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="7fe71-175">-Share</span></span>
<span data-ttu-id="7fe71-176">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="7fe71-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="7fe71-177">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="7fe71-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="7fe71-178">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="7fe71-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="7fe71-179">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="7fe71-179">This object contains the storage context.</span></span>
<span data-ttu-id="7fe71-180">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="7fe71-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe71-181">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="7fe71-181">-ShareName</span></span>
<span data-ttu-id="7fe71-182">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="7fe71-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="7fe71-183">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="7fe71-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="7fe71-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fe71-184">-Confirm</span></span>
<span data-ttu-id="7fe71-185">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fe71-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fe71-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe71-186">-WhatIf</span></span>
<span data-ttu-id="7fe71-187">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fe71-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fe71-188">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fe71-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fe71-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe71-189">CommonParameters</span></span>
<span data-ttu-id="7fe71-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fe71-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe71-191">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fe71-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe71-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fe71-192">INPUTS</span></span>

### <span data-ttu-id="7fe71-193">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="7fe71-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="7fe71-194">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7fe71-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="7fe71-195">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="7fe71-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="7fe71-196">Параметры: Каталог (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7fe71-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="7fe71-197">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="7fe71-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="7fe71-198">Параметры: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7fe71-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="7fe71-199">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fe71-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7fe71-200">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fe71-200">OUTPUTS</span></span>

### <span data-ttu-id="7fe71-201">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="7fe71-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="7fe71-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fe71-202">NOTES</span></span>

## <span data-ttu-id="7fe71-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fe71-203">RELATED LINKS</span></span>

[<span data-ttu-id="7fe71-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="7fe71-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="7fe71-205">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7fe71-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


