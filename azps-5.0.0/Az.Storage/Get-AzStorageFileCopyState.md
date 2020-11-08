---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246355"
---
# <span data-ttu-id="85e51-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="85e51-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="85e51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85e51-102">SYNOPSIS</span></span>
<span data-ttu-id="85e51-103">Получает состояние операции копирования.</span><span class="sxs-lookup"><span data-stu-id="85e51-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="85e51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85e51-104">SYNTAX</span></span>

### <span data-ttu-id="85e51-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="85e51-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="85e51-106">Файл</span><span class="sxs-lookup"><span data-stu-id="85e51-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="85e51-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85e51-107">DESCRIPTION</span></span>
<span data-ttu-id="85e51-108">Командлет **Get-AzStorageFileCopyState** получает состояние операции копирования файлов в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="85e51-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="85e51-109">Оно должно выполняться в конечном файле копирования.</span><span class="sxs-lookup"><span data-stu-id="85e51-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="85e51-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85e51-110">EXAMPLES</span></span>

### <span data-ttu-id="85e51-111">Пример 1: получение состояния копии по имени файла</span><span class="sxs-lookup"><span data-stu-id="85e51-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="85e51-112">Эта команда возвращает состояние операции копирования для файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="85e51-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="85e51-113">Пример 2: Запуск копирования и конвейера для получения состояния копии</span><span class="sxs-lookup"><span data-stu-id="85e51-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="85e51-114">Первая команда запускает копирование файла "contosofile" в "contosofile_copy" и выводит объект destiantion файла.</span><span class="sxs-lookup"><span data-stu-id="85e51-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="85e51-115">Второй командный конвейер для объекта destiantion File для Get-AzStorageFileCopyState, чтобы получить состояние копирования файла.</span><span class="sxs-lookup"><span data-stu-id="85e51-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="85e51-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85e51-116">PARAMETERS</span></span>

### <span data-ttu-id="85e51-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="85e51-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="85e51-118">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="85e51-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="85e51-119">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="85e51-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="85e51-120">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="85e51-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="85e51-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="85e51-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="85e51-122">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="85e51-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="85e51-123">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="85e51-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="85e51-124">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="85e51-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="85e51-125">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="85e51-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="85e51-126">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="85e51-126">The default value is 10.</span></span>

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

### <span data-ttu-id="85e51-127">-Context</span><span class="sxs-lookup"><span data-stu-id="85e51-127">-Context</span></span>
<span data-ttu-id="85e51-128">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="85e51-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="85e51-129">Чтобы получить контекст, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="85e51-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="85e51-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e51-130">-DefaultProfile</span></span>
<span data-ttu-id="85e51-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85e51-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85e51-132">-Файл</span><span class="sxs-lookup"><span data-stu-id="85e51-132">-File</span></span>
<span data-ttu-id="85e51-133">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="85e51-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="85e51-134">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="85e51-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="85e51-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="85e51-135">-FilePath</span></span>
<span data-ttu-id="85e51-136">Задает путь к файлу относительно общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="85e51-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="85e51-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="85e51-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="85e51-138">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="85e51-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="85e51-139">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="85e51-139">-ShareName</span></span>
<span data-ttu-id="85e51-140">Указывает имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="85e51-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="85e51-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="85e51-141">-WaitForComplete</span></span>
<span data-ttu-id="85e51-142">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="85e51-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="85e51-143">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="85e51-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="85e51-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e51-144">CommonParameters</span></span>
<span data-ttu-id="85e51-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85e51-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e51-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e51-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e51-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85e51-147">INPUTS</span></span>

### <span data-ttu-id="85e51-148">Microsoft. Azure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="85e51-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="85e51-149">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="85e51-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="85e51-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85e51-150">OUTPUTS</span></span>

### <span data-ttu-id="85e51-151">Microsoft. Azure. Storage. File. CopyState</span><span class="sxs-lookup"><span data-stu-id="85e51-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="85e51-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="85e51-152">NOTES</span></span>

## <span data-ttu-id="85e51-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85e51-153">RELATED LINKS</span></span>

[<span data-ttu-id="85e51-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="85e51-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="85e51-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="85e51-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="85e51-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="85e51-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="85e51-157">Остановить-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="85e51-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
