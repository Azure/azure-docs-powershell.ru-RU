---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 55a41e03d07cccc30f2cf8193749fcf4096c5179
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910763"
---
# <span data-ttu-id="92d3d-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="92d3d-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="92d3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="92d3d-103">Получает состояние операции копирования.</span><span class="sxs-lookup"><span data-stu-id="92d3d-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="92d3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92d3d-104">SYNTAX</span></span>

### <span data-ttu-id="92d3d-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="92d3d-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="92d3d-106">Файл</span><span class="sxs-lookup"><span data-stu-id="92d3d-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="92d3d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d3d-107">DESCRIPTION</span></span>
<span data-ttu-id="92d3d-108">Командлет **Get-AzStorageFileCopyState** получает состояние операции копирования файлов в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="92d3d-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="92d3d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92d3d-109">EXAMPLES</span></span>

### <span data-ttu-id="92d3d-110">Пример 1: получение состояния копии по имени файла</span><span class="sxs-lookup"><span data-stu-id="92d3d-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="92d3d-111">Эта команда возвращает состояние операции копирования для файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="92d3d-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="92d3d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92d3d-112">PARAMETERS</span></span>

### <span data-ttu-id="92d3d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92d3d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="92d3d-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="92d3d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="92d3d-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="92d3d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="92d3d-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="92d3d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="92d3d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="92d3d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="92d3d-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="92d3d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="92d3d-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="92d3d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="92d3d-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="92d3d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="92d3d-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="92d3d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="92d3d-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="92d3d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="92d3d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="92d3d-123">-Context</span></span>
<span data-ttu-id="92d3d-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="92d3d-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="92d3d-125">Чтобы получить контекст, используйте командлет [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="92d3d-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="92d3d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d3d-126">-DefaultProfile</span></span>
<span data-ttu-id="92d3d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92d3d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d3d-128">-Файл</span><span class="sxs-lookup"><span data-stu-id="92d3d-128">-File</span></span>
<span data-ttu-id="92d3d-129">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="92d3d-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="92d3d-130">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="92d3d-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="92d3d-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="92d3d-131">-FilePath</span></span>
<span data-ttu-id="92d3d-132">Задает путь к файлу относительно общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="92d3d-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="92d3d-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92d3d-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="92d3d-134">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="92d3d-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="92d3d-135">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="92d3d-135">-ShareName</span></span>
<span data-ttu-id="92d3d-136">Указывает имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="92d3d-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="92d3d-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="92d3d-137">-WaitForComplete</span></span>
<span data-ttu-id="92d3d-138">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="92d3d-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="92d3d-139">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="92d3d-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="92d3d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d3d-140">CommonParameters</span></span>
<span data-ttu-id="92d3d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92d3d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d3d-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92d3d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d3d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92d3d-143">INPUTS</span></span>

### <span data-ttu-id="92d3d-144">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="92d3d-144">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="92d3d-145">Параметры: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92d3d-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="92d3d-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="92d3d-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="92d3d-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d3d-147">OUTPUTS</span></span>

### <span data-ttu-id="92d3d-148">Microsoft. WindowsAz. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="92d3d-148">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="92d3d-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="92d3d-149">NOTES</span></span>

## <span data-ttu-id="92d3d-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92d3d-150">RELATED LINKS</span></span>

[<span data-ttu-id="92d3d-151">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="92d3d-151">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="92d3d-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="92d3d-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="92d3d-153">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="92d3d-153">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="92d3d-154">Остановить-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="92d3d-154">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
