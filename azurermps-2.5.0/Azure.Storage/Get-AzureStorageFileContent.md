---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
ms.openlocfilehash: c390a51997e175efb834366a65e10d671f384fa8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913516"
---
# <span data-ttu-id="c5a6e-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c5a6e-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="c5a6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a6e-103">Загружает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5a6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5a6e-104">SYNTAX</span></span>

### <span data-ttu-id="c5a6e-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5a6e-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5a6e-107">Папка</span><span class="sxs-lookup"><span data-stu-id="c5a6e-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5a6e-108">Файл</span><span class="sxs-lookup"><span data-stu-id="c5a6e-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5a6e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-109">DESCRIPTION</span></span>
<span data-ttu-id="c5a6e-110">Командлет **Get-AzureStorageFileContent** загружает содержимое файла, а затем сохраняет его в указанном месте назначения.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="c5a6e-111">Этот командлет не возвращает содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="c5a6e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-112">EXAMPLES</span></span>

### <span data-ttu-id="c5a6e-113">Пример 1: Загрузка файла из папки</span><span class="sxs-lookup"><span data-stu-id="c5a6e-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="c5a6e-114">Эта команда загружает файл с именем CurrentDataFile в папке ContosoWorkingFolder из общей папки ContosoShare06 в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="c5a6e-115">Пример 2: Загрузка файлов в разделе "пример общего файлового файла"</span><span class="sxs-lookup"><span data-stu-id="c5a6e-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="c5a6e-116">В этом примере загружаются файлы из примера общего файлового файла</span><span class="sxs-lookup"><span data-stu-id="c5a6e-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="c5a6e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-117">PARAMETERS</span></span>

### <span data-ttu-id="c5a6e-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="c5a6e-118">-CheckMd5</span></span>
<span data-ttu-id="c5a6e-119">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-120">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-121">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-122">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5a6e-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c5a6e-124">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-125">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-126">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-127">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c5a6e-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c5a6e-129">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-130">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-131">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-132">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-133">-Context</span><span class="sxs-lookup"><span data-stu-id="c5a6e-133">-Context</span></span>
<span data-ttu-id="c5a6e-134">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-135">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-136">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-137">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a6e-138">-DefaultProfile</span></span>
<span data-ttu-id="c5a6e-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5a6e-140">-Destination</span><span class="sxs-lookup"><span data-stu-id="c5a6e-140">-Destination</span></span>
<span data-ttu-id="c5a6e-141">Указывает конечный путь.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-141">Specifies the destination path.</span></span>
<span data-ttu-id="c5a6e-142">Этот командлет загружает содержимое файлов в расположение, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="c5a6e-143">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-144">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-145">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-146">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-147">-Каталог</span><span class="sxs-lookup"><span data-stu-id="c5a6e-147">-Directory</span></span>
<span data-ttu-id="c5a6e-148">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="c5a6e-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="c5a6e-149">Этот командлет получает содержимое файла в папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="c5a6e-150">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="c5a6e-151">Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="c5a6e-152">-Файл</span><span class="sxs-lookup"><span data-stu-id="c5a6e-152">-File</span></span>
<span data-ttu-id="c5a6e-153">Указывает файл как объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="c5a6e-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="c5a6e-154">Этот командлет получает файл, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="c5a6e-155">Чтобы получить объект **CloudFile** , используйте командлет Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="c5a6e-156">-Force</span><span class="sxs-lookup"><span data-stu-id="c5a6e-156">-Force</span></span>
<span data-ttu-id="c5a6e-157">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-158">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-159">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-160">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5a6e-161">-PassThru</span></span>
<span data-ttu-id="c5a6e-162">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-163">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-164">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-165">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-166">-Path</span><span class="sxs-lookup"><span data-stu-id="c5a6e-166">-Path</span></span>
<span data-ttu-id="c5a6e-167">Задает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-167">Specifies the path of a file.</span></span>
<span data-ttu-id="c5a6e-168">Этот командлет получает содержимое файла, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="c5a6e-169">Если файл не существует, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c5a6e-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5a6e-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c5a6e-171">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит содержимое в новом файле.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="c5a6e-172">Если указать путь к уже существующему файлу и задать параметр *Force* , командлет перезапишет файл.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="c5a6e-173">Если вы указали путь к существующему файлу и не указали параметр *Force* , командлет предложит перед продолжением.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="c5a6e-174">Если указать путь к папке, этот командлет попытается создать файл с именем файла хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="c5a6e-175">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-175">-Share</span></span>
<span data-ttu-id="c5a6e-176">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="c5a6e-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="c5a6e-177">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="c5a6e-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="c5a6e-178">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="c5a6e-179">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-179">This object contains the storage context.</span></span>
<span data-ttu-id="c5a6e-180">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="c5a6e-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="c5a6e-181">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="c5a6e-181">-ShareName</span></span>
<span data-ttu-id="c5a6e-182">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="c5a6e-183">Этот командлет загружает содержимое файла в указанном параметре "поделиться".</span><span class="sxs-lookup"><span data-stu-id="c5a6e-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="c5a6e-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5a6e-184">-Confirm</span></span>
<span data-ttu-id="c5a6e-185">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5a6e-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5a6e-186">-WhatIf</span></span>
<span data-ttu-id="c5a6e-187">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5a6e-188">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5a6e-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a6e-189">CommonParameters</span></span>
<span data-ttu-id="c5a6e-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5a6e-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a6e-191">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5a6e-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a6e-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5a6e-192">INPUTS</span></span>

### <span data-ttu-id="c5a6e-193">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c5a6e-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="c5a6e-194">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="c5a6e-195">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="c5a6e-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="c5a6e-196">Параметры: Каталог (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="c5a6e-197">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="c5a6e-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="c5a6e-198">Параметры: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5a6e-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="c5a6e-199">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5a6e-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c5a6e-200">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-200">OUTPUTS</span></span>

### <span data-ttu-id="c5a6e-201">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="c5a6e-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="c5a6e-202">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5a6e-202">NOTES</span></span>

## <span data-ttu-id="c5a6e-203">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5a6e-203">RELATED LINKS</span></span>

[<span data-ttu-id="c5a6e-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c5a6e-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c5a6e-205">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c5a6e-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


