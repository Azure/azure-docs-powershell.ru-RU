---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
ms.openlocfilehash: 5f2aed68aea9f97b3dd66a5322d332d4666c081e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735019"
---
# <span data-ttu-id="19551-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="19551-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="19551-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19551-102">SYNOPSIS</span></span>
<span data-ttu-id="19551-103">Передача содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="19551-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19551-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19551-104">SYNTAX</span></span>

### <span data-ttu-id="19551-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19551-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19551-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="19551-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19551-107">Папка</span><span class="sxs-lookup"><span data-stu-id="19551-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19551-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19551-108">DESCRIPTION</span></span>
<span data-ttu-id="19551-109">Командлет **Set-AzureStorageFileContent** передает содержимое файла в файл в указанной общей папке.</span><span class="sxs-lookup"><span data-stu-id="19551-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="19551-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19551-110">EXAMPLES</span></span>

### <span data-ttu-id="19551-111">Пример 1: Отправка файла в текущей папке</span><span class="sxs-lookup"><span data-stu-id="19551-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="19551-112">Эта команда отправляет файл с именем DataFile37 в текущей папке как файл с именем CurrentDataFile в папке с именем ContosoWorkingFolder.</span><span class="sxs-lookup"><span data-stu-id="19551-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="19551-113">Пример 2: отправка всех файлов в текущей папке</span><span class="sxs-lookup"><span data-stu-id="19551-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="19551-114">В этом примере используются несколько стандартных командлетов Windows PowerShell и текущий командлет для отправки всех файлов из текущей папки в корневую папку контейнера ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="19551-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="19551-115">Первая команда возвращает имя текущей папки и сохраняет ее в переменной $CurrentFolder.</span><span class="sxs-lookup"><span data-stu-id="19551-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="19551-116">Вторая команда использует командлет **Get-AzureStorageShare** для получения общего файлового файла с именем ContosoShare06, а затем сохраняет его в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="19551-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="19551-117">Последняя команда получает содержимое текущей папки и передает каждый из них в командлет Where-Object с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="19551-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="19551-118">Этот командлет отфильтровывает объекты, которые не являются файлами, а затем передает их в командлет ForEach-Object.</span><span class="sxs-lookup"><span data-stu-id="19551-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="19551-119">Этот командлет запускает блок сценария для каждого файла, который создает соответствующий путь для него, и использует текущий командлет для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="19551-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="19551-120">Результат совпадает с именем и относительной позицией, используемой в этом примере для других файлов.</span><span class="sxs-lookup"><span data-stu-id="19551-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="19551-121">Для получения дополнительных сведений о блоках сценариев введите `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="19551-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="19551-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19551-122">PARAMETERS</span></span>

### <span data-ttu-id="19551-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="19551-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="19551-124">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="19551-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="19551-125">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="19551-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="19551-126">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="19551-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="19551-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="19551-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="19551-128">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="19551-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="19551-129">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="19551-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="19551-130">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="19551-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="19551-131">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="19551-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="19551-132">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="19551-132">The default value is 10.</span></span>

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

### <span data-ttu-id="19551-133">-Context</span><span class="sxs-lookup"><span data-stu-id="19551-133">-Context</span></span>
<span data-ttu-id="19551-134">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="19551-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="19551-135">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="19551-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="19551-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="19551-136">-Directory</span></span>
<span data-ttu-id="19551-137">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="19551-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="19551-138">Этот командлет передает файл в папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="19551-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="19551-139">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="19551-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="19551-140">Вы также можете использовать командлет Get-AzureStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="19551-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="19551-141">-Force</span><span class="sxs-lookup"><span data-stu-id="19551-141">-Force</span></span>
<span data-ttu-id="19551-142">Указывает на то, что этот командлет перезапишет существующий файл хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="19551-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="19551-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19551-143">-PassThru</span></span>
<span data-ttu-id="19551-144">Указывает на то, что этот командлет возвращает объект **AzureStorageFile** , который он создает или отправляет.</span><span class="sxs-lookup"><span data-stu-id="19551-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="19551-145">-Path</span><span class="sxs-lookup"><span data-stu-id="19551-145">-Path</span></span>
<span data-ttu-id="19551-146">Задает путь к файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="19551-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="19551-147">Этот командлет передает содержимое в файл, указанный этим параметром, или в файл в папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="19551-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="19551-148">Если указана папка, этот командлет создает файл с тем же именем, что и исходный файл.</span><span class="sxs-lookup"><span data-stu-id="19551-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="19551-149">Если указать путь к файлу, который не существует, этот командлет создаст этот файл и сохранит его содержимое в этом файле.</span><span class="sxs-lookup"><span data-stu-id="19551-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="19551-150">Если вы указали уже существующий файл и задаете параметр _Force_ , этот командлет перезапишет содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="19551-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="19551-151">Если вы указали уже существующий файл и не указали параметр _Force_ , этот командлет не изменится и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="19551-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="19551-152">Если указать путь к папке, которая не существует, этот командлет не изменит и возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="19551-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


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

### <span data-ttu-id="19551-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="19551-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="19551-154">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="19551-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="19551-155">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="19551-155">-Share</span></span>
<span data-ttu-id="19551-156">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="19551-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="19551-157">Этот командлет отправляет файл в файл, общий доступ к которому указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="19551-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="19551-158">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="19551-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="19551-159">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="19551-159">This object contains the storage context.</span></span>
<span data-ttu-id="19551-160">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="19551-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="19551-161">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="19551-161">-ShareName</span></span>
<span data-ttu-id="19551-162">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="19551-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="19551-163">Этот командлет отправляет файл в файл, общий доступ к которому указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="19551-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="19551-164">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="19551-164">-Source</span></span>
<span data-ttu-id="19551-165">Указывает исходный файл, который отправляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="19551-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="19551-166">Если указан несуществующий файл, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="19551-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19551-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19551-167">-Confirm</span></span>
<span data-ttu-id="19551-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19551-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19551-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19551-169">-WhatIf</span></span>
<span data-ttu-id="19551-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19551-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19551-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19551-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19551-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19551-172">CommonParameters</span></span>
<span data-ttu-id="19551-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19551-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19551-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19551-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19551-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19551-175">INPUTS</span></span>

### <span data-ttu-id="19551-176">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="19551-176">IStorageContext</span></span>

<span data-ttu-id="19551-177">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="19551-177">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="19551-178">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="19551-178">CloudFileDirectory</span></span>

<span data-ttu-id="19551-179">Параметр "Directory" принимает значение типа "CloudFileDirectory" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="19551-179">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="19551-180">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="19551-180">CloudFileShare</span></span>

<span data-ttu-id="19551-181">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="19551-181">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="19551-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19551-182">OUTPUTS</span></span>

## <span data-ttu-id="19551-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="19551-183">NOTES</span></span>

## <span data-ttu-id="19551-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19551-184">RELATED LINKS</span></span>

[<span data-ttu-id="19551-185">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="19551-185">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="19551-186">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="19551-186">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="19551-187">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="19551-187">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
