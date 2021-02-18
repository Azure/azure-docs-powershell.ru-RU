---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231633"
---
# <span data-ttu-id="e44c9-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e44c9-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="e44c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e44c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e44c9-103">Список каталогов и файлов для пути.</span><span class="sxs-lookup"><span data-stu-id="e44c9-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="e44c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e44c9-104">SYNTAX</span></span>

### <span data-ttu-id="e44c9-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e44c9-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e44c9-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="e44c9-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e44c9-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="e44c9-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e44c9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e44c9-108">DESCRIPTION</span></span>
<span data-ttu-id="e44c9-109">Для задаваемого вами списка каталогов и файлов для задаваемой папки **Get-AzStorageFile** будет указано ее каталог.</span><span class="sxs-lookup"><span data-stu-id="e44c9-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="e44c9-110">Укажите *параметр Path,* чтобы получить экземпляр каталога или файла в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="e44c9-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="e44c9-111">Этот cmdlet возвращает **объекты AzureStorageFile** и **AzureStorageDirectory.**</span><span class="sxs-lookup"><span data-stu-id="e44c9-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="e44c9-112">С помощью свойства **IsDirectory можно** различать папки и файлы.</span><span class="sxs-lookup"><span data-stu-id="e44c9-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="e44c9-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e44c9-113">EXAMPLES</span></span>

### <span data-ttu-id="e44c9-114">Пример 1. Список каталогов в области</span><span class="sxs-lookup"><span data-stu-id="e44c9-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="e44c9-115">Эта команда содержит только каталоги в share ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e44c9-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="e44c9-116">Он сначала извлекает файлы и каталоги,  передает их в оператор конвейера, а затем удаляет объекты, тип которых не "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="e44c9-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="e44c9-117">Пример 2. Список каталогов файлов</span><span class="sxs-lookup"><span data-stu-id="e44c9-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="e44c9-118">Эта команда содержит список файлов и папок в папке ContosoWorkingFolder каталога ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e44c9-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="e44c9-119">Сначала он получает экземпляр каталога, а затем перена каналает его в список каталогов с его **cmdlet get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="e44c9-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="e44c9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e44c9-120">PARAMETERS</span></span>

### <span data-ttu-id="e44c9-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e44c9-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e44c9-122">Указывает интервал времени времени клиентского времени (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e44c9-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e44c9-123">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="e44c9-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e44c9-124">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e44c9-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e44c9-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e44c9-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e44c9-126">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="e44c9-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e44c9-127">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="e44c9-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e44c9-128">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="e44c9-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e44c9-129">Этот параметр помогает устранять проблемы с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="e44c9-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e44c9-130">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e44c9-130">The default value is 10.</span></span>

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

### <span data-ttu-id="e44c9-131">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e44c9-131">-Context</span></span>
<span data-ttu-id="e44c9-132">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e44c9-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e44c9-133">Чтобы получить контекст хранилища, воспользуйтесь New-AzStorageContext..</span><span class="sxs-lookup"><span data-stu-id="e44c9-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e44c9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e44c9-134">-DefaultProfile</span></span>
<span data-ttu-id="e44c9-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e44c9-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e44c9-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="e44c9-136">-Directory</span></span>
<span data-ttu-id="e44c9-137">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="e44c9-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="e44c9-138">Этот cmdlet возвращает папку, указанную этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e44c9-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="e44c9-139">Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="e44c9-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="e44c9-140">Для получения каталога также можно использовать **cmdlet Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="e44c9-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="e44c9-141">-Path</span><span class="sxs-lookup"><span data-stu-id="e44c9-141">-Path</span></span>
<span data-ttu-id="e44c9-142">Путь к папке.</span><span class="sxs-lookup"><span data-stu-id="e44c9-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="e44c9-143">Если опустить параметр *Path,* **Get-AzStorageFile** выведет список каталогов и файлов в указанной папке или каталоге.</span><span class="sxs-lookup"><span data-stu-id="e44c9-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="e44c9-144">Если включить параметр *Path,* **Get-AzStorageFile** возвращает экземпляр каталога или файла, указанный по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="e44c9-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e44c9-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e44c9-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e44c9-146">Указывает для запроса интервал времени в секундах на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="e44c9-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="e44c9-147">Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="e44c9-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="e44c9-148">-Share</span><span class="sxs-lookup"><span data-stu-id="e44c9-148">-Share</span></span>
<span data-ttu-id="e44c9-149">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="e44c9-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e44c9-150">Этот cmdlet получает файл или каталог из файловой папки, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e44c9-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="e44c9-151">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="e44c9-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="e44c9-152">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="e44c9-152">This object contains the Storage context.</span></span>
<span data-ttu-id="e44c9-153">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="e44c9-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="e44c9-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e44c9-154">-ShareName</span></span>
<span data-ttu-id="e44c9-155">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="e44c9-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="e44c9-156">Этот cmdlet получает файл или каталог из файловой папки, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="e44c9-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="e44c9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e44c9-157">CommonParameters</span></span>
<span data-ttu-id="e44c9-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e44c9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e44c9-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e44c9-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e44c9-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e44c9-160">INPUTS</span></span>

### <span data-ttu-id="e44c9-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e44c9-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e44c9-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="e44c9-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="e44c9-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e44c9-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e44c9-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e44c9-164">OUTPUTS</span></span>

### <span data-ttu-id="e44c9-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e44c9-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="e44c9-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e44c9-166">NOTES</span></span>

## <span data-ttu-id="e44c9-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e44c9-167">RELATED LINKS</span></span>

[<span data-ttu-id="e44c9-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e44c9-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="e44c9-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e44c9-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="e44c9-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e44c9-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="e44c9-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="e44c9-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="e44c9-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e44c9-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


