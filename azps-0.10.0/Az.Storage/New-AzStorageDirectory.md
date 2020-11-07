---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 5582c6459d33096f0427c2b7f6ee237f3c258428
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910725"
---
# <span data-ttu-id="ac3ad-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ac3ad-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="ac3ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3ad-103">Создание каталога.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-103">Creates a directory.</span></span>

## <span data-ttu-id="ac3ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac3ad-104">SYNTAX</span></span>

### <span data-ttu-id="ac3ad-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac3ad-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ac3ad-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac3ad-107">Папка</span><span class="sxs-lookup"><span data-stu-id="ac3ad-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac3ad-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-108">DESCRIPTION</span></span>
<span data-ttu-id="ac3ad-109">Командлет **New-AzStorageDirectory** создает каталог.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="ac3ad-110">Этот командлет возвращает объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="ac3ad-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="ac3ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-111">EXAMPLES</span></span>

### <span data-ttu-id="ac3ad-112">Пример 1: создание папки в общей папке</span><span class="sxs-lookup"><span data-stu-id="ac3ad-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="ac3ad-113">Эта команда создает папку с именем ContosoWorkingFolder в общей папке с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="ac3ad-114">Пример 2: создание папки в общей папке, указанной в объекте "общий доступ к файлам"</span><span class="sxs-lookup"><span data-stu-id="ac3ad-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="ac3ad-115">Эта команда использует командлет **Get-AzStorageShare** для получения общего файлового файла с именем ContosoShare06, а затем передает его в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac3ad-116">Текущий командлет создает папку с именем ContosoWorkingFolder в ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="ac3ad-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-117">PARAMETERS</span></span>

### <span data-ttu-id="ac3ad-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac3ad-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ac3ad-119">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ac3ad-120">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ac3ad-121">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ac3ad-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ac3ad-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ac3ad-123">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ac3ad-124">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ac3ad-125">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ac3ad-126">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ac3ad-127">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-127">The default value is 10.</span></span>

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

### <span data-ttu-id="ac3ad-128">-Context</span><span class="sxs-lookup"><span data-stu-id="ac3ad-128">-Context</span></span>
<span data-ttu-id="ac3ad-129">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ac3ad-130">Чтобы получить контекст хранения, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="ac3ad-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ac3ad-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3ad-131">-DefaultProfile</span></span>
<span data-ttu-id="ac3ad-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac3ad-133">-Каталог</span><span class="sxs-lookup"><span data-stu-id="ac3ad-133">-Directory</span></span>
<span data-ttu-id="ac3ad-134">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="ac3ad-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ac3ad-135">Этот командлет создает папку в том месте, где указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="ac3ad-136">Чтобы получить каталог, используйте командлет New-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="ac3ad-137">Вы также можете использовать командлет Get-AzStorageFile, чтобы получить каталог.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="ac3ad-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ac3ad-138">-Path</span></span>
<span data-ttu-id="ac3ad-139">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="ac3ad-140">Этот командлет создает папку для пути, который указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac3ad-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac3ad-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ac3ad-142">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ac3ad-143">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-143">-Share</span></span>
<span data-ttu-id="ac3ad-144">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="ac3ad-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ac3ad-145">Этот командлет создает папку в общей папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="ac3ad-146">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="ac3ad-147">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-147">This object contains the storage context.</span></span>
<span data-ttu-id="ac3ad-148">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="ac3ad-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="ac3ad-149">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="ac3ad-149">-ShareName</span></span>
<span data-ttu-id="ac3ad-150">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="ac3ad-151">Этот командлет создает папку в общей папке, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac3ad-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3ad-152">CommonParameters</span></span>
<span data-ttu-id="ac3ad-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac3ad-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3ad-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac3ad-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3ad-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac3ad-155">INPUTS</span></span>

### <span data-ttu-id="ac3ad-156">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ac3ad-156">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="ac3ad-157">Параметры: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac3ad-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="ac3ad-158">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="ac3ad-158">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="ac3ad-159">Параметры: Каталог (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac3ad-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="ac3ad-160">System. String</span><span class="sxs-lookup"><span data-stu-id="ac3ad-160">System.String</span></span>

### <span data-ttu-id="ac3ad-161">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac3ad-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac3ad-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-162">OUTPUTS</span></span>

### <span data-ttu-id="ac3ad-163">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="ac3ad-163">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="ac3ad-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac3ad-164">NOTES</span></span>

## <span data-ttu-id="ac3ad-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac3ad-165">RELATED LINKS</span></span>

[<span data-ttu-id="ac3ad-166">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ac3ad-166">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="ac3ad-167">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="ac3ad-167">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="ac3ad-168">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac3ad-168">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ac3ad-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ac3ad-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="ac3ad-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ac3ad-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
