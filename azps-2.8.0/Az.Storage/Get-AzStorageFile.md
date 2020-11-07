---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 5d73923dd3de630673d9228461397ec1789bd268
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907073"
---
# <span data-ttu-id="ac1c0-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ac1c0-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="ac1c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1c0-103">Перечисление каталогов и файлов для пути.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="ac1c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac1c0-104">SYNTAX</span></span>

### <span data-ttu-id="ac1c0-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac1c0-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ac1c0-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac1c0-107">Папка</span><span class="sxs-lookup"><span data-stu-id="ac1c0-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac1c0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-108">DESCRIPTION</span></span>
<span data-ttu-id="ac1c0-109">Командлет **Get-AzStorageFile** выводит список папок и файлов для указанного вами общего доступа или каталога.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="ac1c0-110">Укажите параметр *path* , чтобы получить экземпляр каталога или файла по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="ac1c0-111">Этот командлет возвращает объекты **AzureStorageFile** и **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="ac1c0-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="ac1c0-112">Вы можете использовать свойство " **подкаталог** " для различения папок и файлов.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="ac1c0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-113">EXAMPLES</span></span>

### <span data-ttu-id="ac1c0-114">Пример 1: список папок в общем доступе</span><span class="sxs-lookup"><span data-stu-id="ac1c0-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="ac1c0-115">Эта команда выводит список только для каталогов в ContosoShare06 общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="ac1c0-116">Сначала она извлекает оба файла и каталоги, передает их оператору **WHERE** с помощью оператора конвейера, а затем удаляет все объекты, тип которых не "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="ac1c0-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="ac1c0-117">Пример 2: список папок с файлами</span><span class="sxs-lookup"><span data-stu-id="ac1c0-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="ac1c0-118">Эта команда выводит список файлов и папок в каталоге ContosoWorkingFolder в разделе Общий доступ ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="ac1c0-119">Сначала он получает экземпляр службы каталогов, а затем конвейер в командлет **Get-AzStorageFile для получения** списка каталогов.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="ac1c0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-120">PARAMETERS</span></span>

### <span data-ttu-id="ac1c0-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac1c0-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ac1c0-122">Указывает интервал времени ожидания для одного запроса службы (в секундах).</span><span class="sxs-lookup"><span data-stu-id="ac1c0-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ac1c0-123">Если предыдущий вызов завершается сбоем в течение указанного интервала, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ac1c0-124">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ac1c0-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ac1c0-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ac1c0-126">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ac1c0-127">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ac1c0-128">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ac1c0-129">Этот параметр помогает уменьшить число проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ac1c0-130">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-130">The default value is 10.</span></span>

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

### <span data-ttu-id="ac1c0-131">-Context</span><span class="sxs-lookup"><span data-stu-id="ac1c0-131">-Context</span></span>
<span data-ttu-id="ac1c0-132">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ac1c0-133">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ac1c0-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1c0-134">-DefaultProfile</span></span>
<span data-ttu-id="ac1c0-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac1c0-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="ac1c0-136">-Directory</span></span>
<span data-ttu-id="ac1c0-137">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="ac1c0-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ac1c0-138">Этот командлет получает папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="ac1c0-139">Чтобы получить каталог, используйте командлет New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="ac1c0-140">Вы также можете использовать командлет **Get-AzStorageFile** , чтобы получить доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1c0-141">-Path</span><span class="sxs-lookup"><span data-stu-id="ac1c0-141">-Path</span></span>
<span data-ttu-id="ac1c0-142">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="ac1c0-143">Если параметр *путь* не указан, **Get-AzStorageFile** приводит к перечислению каталогов и файлов в указанной общей папке или в каталоге.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="ac1c0-144">Если вы включаете параметр *path* , функция **Get-AzStorageFile** возвращает экземпляр каталога или файла в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="ac1c0-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac1c0-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ac1c0-146">Задает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="ac1c0-147">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="ac1c0-148">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-148">-Share</span></span>
<span data-ttu-id="ac1c0-149">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="ac1c0-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ac1c0-150">Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="ac1c0-151">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="ac1c0-152">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-152">This object contains the Storage context.</span></span>
<span data-ttu-id="ac1c0-153">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="ac1c0-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac1c0-154">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="ac1c0-154">-ShareName</span></span>
<span data-ttu-id="ac1c0-155">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="ac1c0-156">Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac1c0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1c0-157">CommonParameters</span></span>
<span data-ttu-id="ac1c0-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac1c0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1c0-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac1c0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1c0-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac1c0-160">INPUTS</span></span>

### <span data-ttu-id="ac1c0-161">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ac1c0-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="ac1c0-162">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="ac1c0-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="ac1c0-163">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac1c0-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac1c0-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-164">OUTPUTS</span></span>

### <span data-ttu-id="ac1c0-165">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="ac1c0-165">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="ac1c0-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac1c0-166">NOTES</span></span>

## <span data-ttu-id="ac1c0-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac1c0-167">RELATED LINKS</span></span>

[<span data-ttu-id="ac1c0-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ac1c0-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="ac1c0-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ac1c0-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="ac1c0-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ac1c0-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="ac1c0-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ac1c0-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="ac1c0-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ac1c0-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


