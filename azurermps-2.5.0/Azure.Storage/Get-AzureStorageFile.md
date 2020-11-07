---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
ms.openlocfilehash: fac810fe1c58a7be18204f51b0f124a490196edc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913517"
---
# <span data-ttu-id="0553e-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0553e-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="0553e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0553e-102">SYNOPSIS</span></span>
<span data-ttu-id="0553e-103">Перечисление каталогов и файлов для пути.</span><span class="sxs-lookup"><span data-stu-id="0553e-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0553e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0553e-104">SYNTAX</span></span>

### <span data-ttu-id="0553e-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0553e-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0553e-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="0553e-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0553e-107">Папка</span><span class="sxs-lookup"><span data-stu-id="0553e-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="0553e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0553e-108">DESCRIPTION</span></span>
<span data-ttu-id="0553e-109">Командлет **Get-AzureStorageFile** выводит список папок и файлов для указанного вами общего доступа или каталога.</span><span class="sxs-lookup"><span data-stu-id="0553e-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="0553e-110">Укажите параметр *path* , чтобы получить экземпляр каталога или файла по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="0553e-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="0553e-111">Этот командлет возвращает объекты **AzureStorageFile** и **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="0553e-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="0553e-112">Вы можете использовать свойство " **подкаталог** " для различения папок и файлов.</span><span class="sxs-lookup"><span data-stu-id="0553e-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="0553e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0553e-113">EXAMPLES</span></span>

### <span data-ttu-id="0553e-114">Пример 1: список папок в общем доступе</span><span class="sxs-lookup"><span data-stu-id="0553e-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="0553e-115">Эта команда выводит список только для каталогов в ContosoShare06 общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0553e-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="0553e-116">Сначала она извлекает оба файла и каталоги, передает их оператору **WHERE** с помощью оператора конвейера, а затем удаляет все объекты, тип которых не "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="0553e-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="0553e-117">Пример 2: список папок с файлами</span><span class="sxs-lookup"><span data-stu-id="0553e-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="0553e-118">Эта команда выводит список файлов и папок в каталоге ContosoWorkingFolder в разделе Общий доступ ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="0553e-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="0553e-119">Сначала он получает экземпляр службы каталогов, а затем конвейер в командлет **Get-AzureStorageFile для получения** списка каталогов.</span><span class="sxs-lookup"><span data-stu-id="0553e-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="0553e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0553e-120">PARAMETERS</span></span>

### <span data-ttu-id="0553e-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0553e-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0553e-122">Указывает интервал времени ожидания для одного запроса службы (в секундах).</span><span class="sxs-lookup"><span data-stu-id="0553e-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0553e-123">Если предыдущий вызов завершается сбоем в течение указанного интервала, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="0553e-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0553e-124">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0553e-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0553e-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0553e-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0553e-126">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0553e-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0553e-127">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="0553e-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0553e-128">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="0553e-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0553e-129">Этот параметр помогает уменьшить число проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="0553e-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0553e-130">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0553e-130">The default value is 10.</span></span>

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

### <span data-ttu-id="0553e-131">-Context</span><span class="sxs-lookup"><span data-stu-id="0553e-131">-Context</span></span>
<span data-ttu-id="0553e-132">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0553e-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0553e-133">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0553e-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0553e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0553e-134">-DefaultProfile</span></span>
<span data-ttu-id="0553e-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0553e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0553e-136">-Каталог</span><span class="sxs-lookup"><span data-stu-id="0553e-136">-Directory</span></span>
<span data-ttu-id="0553e-137">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="0553e-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="0553e-138">Этот командлет получает папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="0553e-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="0553e-139">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="0553e-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="0553e-140">Вы также можете использовать командлет **Get-AzureStorageFile** , чтобы получить доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="0553e-140">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="0553e-141">-Path</span><span class="sxs-lookup"><span data-stu-id="0553e-141">-Path</span></span>
<span data-ttu-id="0553e-142">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="0553e-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="0553e-143">Если параметр *путь* не указан, **Get-AzureStorageFile** приводит к перечислению каталогов и файлов в указанной общей папке или в каталоге.</span><span class="sxs-lookup"><span data-stu-id="0553e-143">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="0553e-144">Если вы включаете параметр *path* , функция **Get-AzureStorageFile** возвращает экземпляр каталога или файла в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="0553e-144">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

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

### <span data-ttu-id="0553e-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0553e-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0553e-146">Задает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="0553e-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="0553e-147">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0553e-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="0553e-148">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="0553e-148">-Share</span></span>
<span data-ttu-id="0553e-149">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="0553e-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="0553e-150">Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0553e-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="0553e-151">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="0553e-151">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="0553e-152">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="0553e-152">This object contains the Storage context.</span></span>
<span data-ttu-id="0553e-153">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="0553e-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="0553e-154">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="0553e-154">-ShareName</span></span>
<span data-ttu-id="0553e-155">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="0553e-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="0553e-156">Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0553e-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="0553e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0553e-157">CommonParameters</span></span>
<span data-ttu-id="0553e-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0553e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0553e-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0553e-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0553e-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0553e-160">INPUTS</span></span>

### <span data-ttu-id="0553e-161">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0553e-161">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="0553e-162">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0553e-162">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="0553e-163">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0553e-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="0553e-164">Параметры: Каталог (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0553e-164">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="0553e-165">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0553e-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0553e-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0553e-166">OUTPUTS</span></span>

### <span data-ttu-id="0553e-167">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="0553e-167">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="0553e-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="0553e-168">NOTES</span></span>

## <span data-ttu-id="0553e-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0553e-169">RELATED LINKS</span></span>

[<span data-ttu-id="0553e-170">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0553e-170">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="0553e-171">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0553e-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="0553e-172">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="0553e-172">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="0553e-173">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="0553e-173">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="0553e-174">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0553e-174">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


