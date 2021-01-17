---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419999"
---
# <span data-ttu-id="6dd8e-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6dd8e-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="6dd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd8e-103">Отправка содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="6dd8e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6dd8e-104">SYNTAX</span></span>

### <span data-ttu-id="6dd8e-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6dd8e-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="6dd8e-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="6dd8e-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="6dd8e-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="6dd8e-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="6dd8e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dd8e-108">DESCRIPTION</span></span>
<span data-ttu-id="6dd8e-109">Для отправки содержимого файла в файл в указанной папке будет добавлено содержимое файла в папке **Set-AzStorageFileContent.**</span><span class="sxs-lookup"><span data-stu-id="6dd8e-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="6dd8e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6dd8e-110">EXAMPLES</span></span>

### <span data-ttu-id="6dd8e-111">Пример 1. Отправка файла в текущую папку</span><span class="sxs-lookup"><span data-stu-id="6dd8e-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="6dd8e-112">Эта команда передает файл с именем DataFile37 в текущей папке в качестве файла CurrentDataFile в папке ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="6dd8e-113">Пример 2. Отправка всех файлов в текущую папку</span><span class="sxs-lookup"><span data-stu-id="6dd8e-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="6dd8e-114">В этом примере используются Windows PowerShell и текущий для добавления всех файлов из текущей папки в корневую папку контейнера ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="6dd8e-115">Первая команда получает имя текущей папки и сохраняет ее в переменной $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="6dd8e-116">Вторая команда использует командлет **Get-AzStorageShare,** чтобы получить файл с именем ContosoShare06, а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6dd8e-117">Конечная команда получает содержимое текущей папки и передает каждую из них в командлет Where-Object с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6dd8e-118">Он фильтрует объекты, которые не являются файлами, а затем передает файлы в ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="6dd8e-119">Этот cmdlet запускает блок сценария для каждого файла, который создает соответствующий путь для него, а затем использует текущий для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="6dd8e-120">Результат имеет то же имя и относительную позицию относительно других файлов, которые загружаются в этом примере.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="6dd8e-121">Чтобы получить дополнительные сведения о блоках сценариев, введите `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="6dd8e-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="6dd8e-122">Пример 3. Вы можете добавить локальный файл в файл Azure и заявить его свойства (File Attributtes), время создания файла, время последней записи файла в файле Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="6dd8e-123">В этом примере локальный файл загружается в файл Azure, а его свойства (File Attributtes), время создания файла, время последней записи файла) в файле Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="6dd8e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dd8e-124">PARAMETERS</span></span>

### <span data-ttu-id="6dd8e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6dd8e-125">-AsJob</span></span>
<span data-ttu-id="6dd8e-126">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6dd8e-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6dd8e-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6dd8e-128">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6dd8e-129">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6dd8e-130">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6dd8e-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6dd8e-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6dd8e-132">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6dd8e-133">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6dd8e-134">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6dd8e-135">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6dd8e-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-136">The default value is 10.</span></span>

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

### <span data-ttu-id="6dd8e-137">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6dd8e-137">-Context</span></span>
<span data-ttu-id="6dd8e-138">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6dd8e-139">Чтобы получить контекст хранилища, воспользуйтесь [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="6dd8e-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6dd8e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd8e-140">-DefaultProfile</span></span>
<span data-ttu-id="6dd8e-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dd8e-142">-Каталог</span><span class="sxs-lookup"><span data-stu-id="6dd8e-142">-Directory</span></span>
<span data-ttu-id="6dd8e-143">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="6dd8e-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="6dd8e-144">Этот cmdlet передает файл в папку, указанную этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="6dd8e-145">Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="6dd8e-146">Для получения каталога Get-AzStorageFile можно также воспользоваться этим Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="6dd8e-147">-Force</span><span class="sxs-lookup"><span data-stu-id="6dd8e-147">-Force</span></span>
<span data-ttu-id="6dd8e-148">Указывает на то, что этот cmdlet переопишет существующий файл хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="6dd8e-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dd8e-149">-PassThru</span></span>
<span data-ttu-id="6dd8e-150">Указывает на то, что этот cmdlet возвращает объект **AzureStorageFile,** который он создает или передает.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="6dd8e-151">-Path</span><span class="sxs-lookup"><span data-stu-id="6dd8e-151">-Path</span></span>
<span data-ttu-id="6dd8e-152">Путь к файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="6dd8e-153">Этот cmdlet передает содержимое в файл, указанный этим параметром, или в файл в папке, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="6dd8e-154">При указании папки этот cmdlet создает файл с тем же именем, что и у источника.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="6dd8e-155">Если указать путь к файлу, который не существует, этот cmdlet создаст этот файл и сохранит его содержимое.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="6dd8e-156">Если указать файл, который уже существует, и задать параметр _Force,_ этот cmdlet переопишет его содержимое.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="6dd8e-157">Если указать файл, который уже существует, а не "Принудительно", этот cmdlet не будет изменяться и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="6dd8e-158">Если указать путь к не существует папке, этот cmdlet не будет изменяться и возвратит ошибку.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="6dd8e-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="6dd8e-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="6dd8e-160">Сохранить исходные свойства SMB-файла (File Attributtes, время создания файла, время последней записи файла) в нужном файле.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="6dd8e-161">Этот параметр доступен только в Windows.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="6dd8e-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6dd8e-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6dd8e-163">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6dd8e-164">-Share</span><span class="sxs-lookup"><span data-stu-id="6dd8e-164">-Share</span></span>
<span data-ttu-id="6dd8e-165">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="6dd8e-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="6dd8e-166">Этот cmdlet передается в файл в папке с файлом, который определяет этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="6dd8e-167">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="6dd8e-168">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-168">This object contains the storage context.</span></span>
<span data-ttu-id="6dd8e-169">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="6dd8e-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="6dd8e-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6dd8e-170">-ShareName</span></span>
<span data-ttu-id="6dd8e-171">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="6dd8e-172">Этот cmdlet передается в файл в папке с файлом, который определяет этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="6dd8e-173">-Source</span><span class="sxs-lookup"><span data-stu-id="6dd8e-173">-Source</span></span>
<span data-ttu-id="6dd8e-174">Определяет исходный файл, который будет добавлен этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="6dd8e-175">Если указать файл, который не существует, этот cmdlet возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dd8e-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dd8e-176">-Confirm</span></span>
<span data-ttu-id="6dd8e-177">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd8e-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd8e-178">-WhatIf</span></span>
<span data-ttu-id="6dd8e-179">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd8e-180">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd8e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd8e-181">CommonParameters</span></span>
<span data-ttu-id="6dd8e-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd8e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd8e-183">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dd8e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd8e-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dd8e-184">INPUTS</span></span>

### <span data-ttu-id="6dd8e-185">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="6dd8e-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="6dd8e-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="6dd8e-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="6dd8e-187">System.String</span><span class="sxs-lookup"><span data-stu-id="6dd8e-187">System.String</span></span>

### <span data-ttu-id="6dd8e-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6dd8e-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6dd8e-189">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6dd8e-189">OUTPUTS</span></span>

### <span data-ttu-id="6dd8e-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6dd8e-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="6dd8e-191">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6dd8e-191">NOTES</span></span>

## <span data-ttu-id="6dd8e-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dd8e-192">RELATED LINKS</span></span>

[<span data-ttu-id="6dd8e-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="6dd8e-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="6dd8e-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="6dd8e-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="6dd8e-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6dd8e-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
