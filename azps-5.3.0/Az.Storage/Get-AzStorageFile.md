---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504665"
---
# <span data-ttu-id="cf7ec-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cf7ec-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="cf7ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7ec-103">Список каталогов и файлов для пути.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="cf7ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf7ec-104">SYNTAX</span></span>

### <span data-ttu-id="cf7ec-105">ShareName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf7ec-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cf7ec-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="cf7ec-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf7ec-107">Каталог</span><span class="sxs-lookup"><span data-stu-id="cf7ec-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf7ec-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf7ec-108">DESCRIPTION</span></span>
<span data-ttu-id="cf7ec-109">Для задаваемого списка каталогов можно задать список каталогов и файлов для задаваемой вами папки **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="cf7ec-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="cf7ec-110">Укажите *параметр Path,* чтобы получить экземпляр каталога или файла в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="cf7ec-111">Этот cmdlet возвращает **объекты AzureStorageFile** и **AzureStorageDirectory.**</span><span class="sxs-lookup"><span data-stu-id="cf7ec-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="cf7ec-112">С помощью свойства **IsDirectory можно** различать папки и файлы.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="cf7ec-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf7ec-113">EXAMPLES</span></span>

### <span data-ttu-id="cf7ec-114">Пример 1. Список каталогов в области</span><span class="sxs-lookup"><span data-stu-id="cf7ec-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="cf7ec-115">Эта команда содержит только каталоги в share ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="cf7ec-116">Он сначала извлекает файлы и каталоги,  передает их оператору конвейера, а затем удаляет объекты, тип которых не "AzureStorageFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="cf7ec-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="cf7ec-117">Пример 2. Список каталогов файлов</span><span class="sxs-lookup"><span data-stu-id="cf7ec-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="cf7ec-118">Эта команда содержит список файлов и папок в папке ContosoWorkingFolder каталога ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="cf7ec-119">Сначала он получает экземпляр каталога, а затем перена каналает его в список каталогов с cmdlet **Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="cf7ec-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="cf7ec-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf7ec-120">PARAMETERS</span></span>

### <span data-ttu-id="cf7ec-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf7ec-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf7ec-122">Указывает интервал времени времени клиентского времени (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf7ec-123">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf7ec-124">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf7ec-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf7ec-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf7ec-126">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf7ec-127">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf7ec-128">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf7ec-129">Этот параметр помогает устранять проблемы с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf7ec-130">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-130">The default value is 10.</span></span>

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

### <span data-ttu-id="cf7ec-131">-Контекст</span><span class="sxs-lookup"><span data-stu-id="cf7ec-131">-Context</span></span>
<span data-ttu-id="cf7ec-132">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="cf7ec-133">Чтобы получить контекст хранилища, воспользуйтесь New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cf7ec-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7ec-134">-DefaultProfile</span></span>
<span data-ttu-id="cf7ec-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf7ec-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="cf7ec-136">-Directory</span></span>
<span data-ttu-id="cf7ec-137">Указывает папку как объект **CloudFileDirectory.**</span><span class="sxs-lookup"><span data-stu-id="cf7ec-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="cf7ec-138">Этот cmdlet возвращает папку, указанную этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="cf7ec-139">Чтобы получить каталог, воспользуйтесь New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="cf7ec-140">Для получения каталога также можно использовать **cmdlet Get-AzStorageFile.**</span><span class="sxs-lookup"><span data-stu-id="cf7ec-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="cf7ec-141">-Path</span><span class="sxs-lookup"><span data-stu-id="cf7ec-141">-Path</span></span>
<span data-ttu-id="cf7ec-142">Путь к папке.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="cf7ec-143">Если опустить параметр *Path,* **Get-AzStorageFile** выведет список каталогов и файлов в указанной папке или каталоге.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="cf7ec-144">Если включить параметр *Path,* **Get-AzStorageFile** возвращает экземпляр каталога или файла, указанный по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="cf7ec-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf7ec-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf7ec-146">Указывает для запроса интервал времени в секундах на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="cf7ec-147">Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="cf7ec-148">-Share</span><span class="sxs-lookup"><span data-stu-id="cf7ec-148">-Share</span></span>
<span data-ttu-id="cf7ec-149">Указывает объект **CloudFileShare.**</span><span class="sxs-lookup"><span data-stu-id="cf7ec-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="cf7ec-150">Этот cmdlet получает файл или каталог из папки, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="cf7ec-151">Чтобы получить объект **CloudFileShare,** воспользуйтесь Get-AzStorageShare управления.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="cf7ec-152">Этот объект содержит контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-152">This object contains the Storage context.</span></span>
<span data-ttu-id="cf7ec-153">Если вы указали этот параметр, не укажите параметр *Context.*</span><span class="sxs-lookup"><span data-stu-id="cf7ec-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="cf7ec-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="cf7ec-154">-ShareName</span></span>
<span data-ttu-id="cf7ec-155">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="cf7ec-156">Этот cmdlet получает файл или каталог из папки, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="cf7ec-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7ec-157">CommonParameters</span></span>
<span data-ttu-id="cf7ec-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf7ec-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7ec-159">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf7ec-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7ec-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf7ec-160">INPUTS</span></span>

### <span data-ttu-id="cf7ec-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="cf7ec-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="cf7ec-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="cf7ec-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="cf7ec-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cf7ec-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cf7ec-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf7ec-164">OUTPUTS</span></span>

### <span data-ttu-id="cf7ec-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="cf7ec-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="cf7ec-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf7ec-166">NOTES</span></span>

## <span data-ttu-id="cf7ec-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf7ec-167">RELATED LINKS</span></span>

[<span data-ttu-id="cf7ec-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cf7ec-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="cf7ec-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cf7ec-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="cf7ec-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="cf7ec-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="cf7ec-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="cf7ec-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="cf7ec-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cf7ec-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


