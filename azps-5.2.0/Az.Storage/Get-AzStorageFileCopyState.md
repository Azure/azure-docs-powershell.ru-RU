---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324984"
---
# <span data-ttu-id="d8cdf-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="d8cdf-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="d8cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cdf-103">Состояние копирования.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="d8cdf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8cdf-104">SYNTAX</span></span>

### <span data-ttu-id="d8cdf-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="d8cdf-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d8cdf-106">Файл</span><span class="sxs-lookup"><span data-stu-id="d8cdf-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8cdf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8cdf-107">DESCRIPTION</span></span>
<span data-ttu-id="d8cdf-108">Для получения состояния операции копирования файлов хранилища Azure возвращается состояние операции **get-AzStorageFileCopyState.**</span><span class="sxs-lookup"><span data-stu-id="d8cdf-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="d8cdf-109">Оно должно запуститься в файле назначения для копирования.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="d8cdf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8cdf-110">EXAMPLES</span></span>

### <span data-ttu-id="d8cdf-111">Пример 1. Просмотр состояния копии по имени файла</span><span class="sxs-lookup"><span data-stu-id="d8cdf-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="d8cdf-112">Эта команда возвращает состояние операции копирования для файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="d8cdf-113">Пример 2. Запуск копирования и конвейер для получения состояния копии</span><span class="sxs-lookup"><span data-stu-id="d8cdf-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="d8cdf-114">Первая команда начинает копировать файл "contosofile" в "contosofile_copy" и выводит объект файла destiantion.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="d8cdf-115">Второй канал команд для получения состояния копирования файла destiantion до Get-AzStorageFileCopyState.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="d8cdf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8cdf-116">PARAMETERS</span></span>

### <span data-ttu-id="d8cdf-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8cdf-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d8cdf-118">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d8cdf-119">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d8cdf-120">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d8cdf-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d8cdf-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d8cdf-122">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d8cdf-123">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d8cdf-124">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d8cdf-125">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d8cdf-126">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-126">The default value is 10.</span></span>

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

### <span data-ttu-id="d8cdf-127">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d8cdf-127">-Context</span></span>
<span data-ttu-id="d8cdf-128">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d8cdf-129">Для получения контекста используйте [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="d8cdf-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d8cdf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cdf-130">-DefaultProfile</span></span>
<span data-ttu-id="d8cdf-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8cdf-132">-File</span><span class="sxs-lookup"><span data-stu-id="d8cdf-132">-File</span></span>
<span data-ttu-id="d8cdf-133">Указывает объект **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="d8cdf-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d8cdf-134">Вы можете создать облачный файл или получить его с помощью Get-AzStorageFile-файла.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8cdf-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d8cdf-135">-FilePath</span></span>
<span data-ttu-id="d8cdf-136">Путь к файлу относительно папки хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cdf-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8cdf-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d8cdf-138">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d8cdf-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d8cdf-139">-ShareName</span></span>
<span data-ttu-id="d8cdf-140">Указывает имя поделиться.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="d8cdf-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d8cdf-141">-WaitForComplete</span></span>
<span data-ttu-id="d8cdf-142">Указывает на то, что этот cmdlet ждет завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="d8cdf-143">Если этот параметр не задан, этот cmdlet возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="d8cdf-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cdf-144">CommonParameters</span></span>
<span data-ttu-id="d8cdf-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cdf-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cdf-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cdf-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cdf-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8cdf-147">INPUTS</span></span>

### <span data-ttu-id="d8cdf-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="d8cdf-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="d8cdf-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8cdf-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d8cdf-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8cdf-150">OUTPUTS</span></span>

### <span data-ttu-id="d8cdf-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="d8cdf-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="d8cdf-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8cdf-152">NOTES</span></span>

## <span data-ttu-id="d8cdf-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8cdf-153">RELATED LINKS</span></span>

[<span data-ttu-id="d8cdf-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d8cdf-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="d8cdf-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8cdf-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d8cdf-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d8cdf-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="d8cdf-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d8cdf-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
