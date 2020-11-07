---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: e6d5bcad88e50fcd166e2d7a8c37ca948ae355f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910775"
---
# <span data-ttu-id="4e115-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="4e115-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="4e115-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e115-102">SYNOPSIS</span></span>
<span data-ttu-id="4e115-103">Получает состояние копии большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e115-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="4e115-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e115-104">SYNTAX</span></span>

### <span data-ttu-id="4e115-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e115-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4e115-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="4e115-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4e115-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="4e115-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4e115-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e115-108">DESCRIPTION</span></span>
<span data-ttu-id="4e115-109">Командлет **Get-AzStorageBlobCopyState** получает состояние копии большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e115-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="4e115-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e115-110">EXAMPLES</span></span>

### <span data-ttu-id="4e115-111">Пример 1: получение состояния копии большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="4e115-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="4e115-112">Эта команда возвращает состояние копирования большого двоичного объекта с именем ContosoPlanning2015 в контейнере ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="4e115-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="4e115-113">Пример 2: получение состояния копии для большого двоичного объекта с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="4e115-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="4e115-114">Эта команда получает двоичный объект с именем ContosoPlanning2015 в контейнере с именем ContosoUploads с помощью командлета **Get-AzStorageBlob** , а затем передает результат в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="4e115-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4e115-115">Командлет **Get-AzStorageBlobCopyState** получает состояние копирования для этого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4e115-115">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="4e115-116">Пример 3: получение состояния копии для большого двоичного объекта в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="4e115-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="4e115-117">Эта команда получает контейнер с именем с помощью командлета **Get-AzStorageBlob** , а затем передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="4e115-117">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="4e115-118">Командлет **Get-AzStorageContainer** получает состояние копирования для большого двоичного объекта с именем ContosoPlanning2015 в этом контейнере.</span><span class="sxs-lookup"><span data-stu-id="4e115-118">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="4e115-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e115-119">PARAMETERS</span></span>

### <span data-ttu-id="4e115-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="4e115-120">-Blob</span></span>
<span data-ttu-id="4e115-121">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="4e115-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="4e115-122">Этот командлет получает состояние операции копирования BLOB-объектов хранилища Azure, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4e115-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e115-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e115-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4e115-124">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="4e115-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4e115-125">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="4e115-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4e115-126">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4e115-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4e115-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4e115-127">-CloudBlob</span></span>
<span data-ttu-id="4e115-128">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e115-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="4e115-129">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="4e115-129">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e115-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4e115-130">-CloudBlobContainer</span></span>
<span data-ttu-id="4e115-131">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e115-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="4e115-132">Этот командлет получает состояние копирования большого двоичного объекта в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4e115-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="4e115-133">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="4e115-133">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e115-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4e115-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4e115-135">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4e115-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4e115-136">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="4e115-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4e115-137">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="4e115-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4e115-138">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="4e115-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4e115-139">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="4e115-139">The default value is 10.</span></span>

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

### <span data-ttu-id="4e115-140">-Container</span><span class="sxs-lookup"><span data-stu-id="4e115-140">-Container</span></span>
<span data-ttu-id="4e115-141">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="4e115-141">Specifies the name of a container.</span></span>
<span data-ttu-id="4e115-142">Этот командлет получает состояние копирования для большого двоичного объекта в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="4e115-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e115-143">-Context</span><span class="sxs-lookup"><span data-stu-id="4e115-143">-Context</span></span>
<span data-ttu-id="4e115-144">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4e115-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4e115-145">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4e115-145">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e115-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e115-146">-DefaultProfile</span></span>
<span data-ttu-id="4e115-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e115-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e115-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4e115-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4e115-149">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="4e115-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="4e115-150">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="4e115-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="4e115-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="4e115-151">-WaitForComplete</span></span>
<span data-ttu-id="4e115-152">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="4e115-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="4e115-153">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="4e115-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="4e115-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e115-154">CommonParameters</span></span>
<span data-ttu-id="4e115-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e115-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e115-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e115-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e115-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e115-157">INPUTS</span></span>

### <span data-ttu-id="4e115-158">Microsoft. WindowsAz. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="4e115-158">Microsoft.WindowsAz.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="4e115-159">Microsoft. WindowsAz. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="4e115-159">Microsoft.WindowsAz.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="4e115-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4e115-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4e115-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e115-161">OUTPUTS</span></span>

### <span data-ttu-id="4e115-162">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="4e115-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="4e115-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e115-163">NOTES</span></span>

## <span data-ttu-id="4e115-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e115-164">RELATED LINKS</span></span>

[<span data-ttu-id="4e115-165">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4e115-165">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="4e115-166">Остановить-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4e115-166">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


