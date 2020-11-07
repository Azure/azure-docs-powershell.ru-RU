---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
ms.openlocfilehash: 3b74b1f68bf6bb990f76d18b73f113e6a0f8e446
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913949"
---
# <span data-ttu-id="50770-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="50770-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="50770-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50770-102">SYNOPSIS</span></span>
<span data-ttu-id="50770-103">Получает состояние копии большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="50770-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50770-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50770-104">SYNTAX</span></span>

### <span data-ttu-id="50770-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50770-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="50770-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="50770-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="50770-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="50770-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="50770-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50770-108">DESCRIPTION</span></span>
<span data-ttu-id="50770-109">Командлет **Get-AzureStorageBlobCopyState** получает состояние копии большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="50770-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="50770-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50770-110">EXAMPLES</span></span>

### <span data-ttu-id="50770-111">Пример 1: получение состояния копии большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="50770-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="50770-112">Эта команда возвращает состояние копирования большого двоичного объекта с именем ContosoPlanning2015 в контейнере ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="50770-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="50770-113">Пример 2: получение состояния копии для большого двоичного объекта с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="50770-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="50770-114">Эта команда получает двоичный объект с именем ContosoPlanning2015 в контейнере с именем ContosoUploads с помощью командлета **Get-AzureStorageBlob** , а затем передает результат в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="50770-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50770-115">Командлет **Get-AzureStorageBlobCopyState** получает состояние копирования для этого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="50770-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="50770-116">Пример 3: получение состояния копии для большого двоичного объекта в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="50770-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="50770-117">Эта команда получает контейнер с именем с помощью командлета **Get-AzureStorageBlob** , а затем передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="50770-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="50770-118">Командлет **Get-AzureStorageContainer** получает состояние копирования для большого двоичного объекта с именем ContosoPlanning2015 в этом контейнере.</span><span class="sxs-lookup"><span data-stu-id="50770-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="50770-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50770-119">PARAMETERS</span></span>

### <span data-ttu-id="50770-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="50770-120">-Blob</span></span>
<span data-ttu-id="50770-121">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="50770-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="50770-122">Этот командлет получает состояние операции копирования BLOB-объектов хранилища Azure, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="50770-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="50770-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="50770-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="50770-124">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="50770-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="50770-125">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="50770-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="50770-126">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="50770-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="50770-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="50770-127">-CloudBlob</span></span>
<span data-ttu-id="50770-128">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="50770-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="50770-129">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="50770-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50770-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="50770-130">-CloudBlobContainer</span></span>
<span data-ttu-id="50770-131">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="50770-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="50770-132">Этот командлет получает состояние копирования большого двоичного объекта в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="50770-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="50770-133">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="50770-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50770-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="50770-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="50770-135">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="50770-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="50770-136">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="50770-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="50770-137">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="50770-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="50770-138">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="50770-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="50770-139">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="50770-139">The default value is 10.</span></span>

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

### <span data-ttu-id="50770-140">-Container</span><span class="sxs-lookup"><span data-stu-id="50770-140">-Container</span></span>
<span data-ttu-id="50770-141">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="50770-141">Specifies the name of a container.</span></span>
<span data-ttu-id="50770-142">Этот командлет получает состояние копирования для большого двоичного объекта в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="50770-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="50770-143">-Context</span><span class="sxs-lookup"><span data-stu-id="50770-143">-Context</span></span>
<span data-ttu-id="50770-144">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="50770-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="50770-145">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="50770-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="50770-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50770-146">-DefaultProfile</span></span>
<span data-ttu-id="50770-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50770-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50770-148">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="50770-148">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="50770-149">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="50770-149">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="50770-150">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="50770-150">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="50770-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="50770-151">-WaitForComplete</span></span>
<span data-ttu-id="50770-152">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="50770-152">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="50770-153">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="50770-153">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="50770-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50770-154">CommonParameters</span></span>
<span data-ttu-id="50770-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50770-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50770-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50770-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50770-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50770-157">INPUTS</span></span>

### <span data-ttu-id="50770-158">Microsoft. WindowsAzure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="50770-158">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="50770-159">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="50770-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="50770-160">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="50770-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="50770-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50770-161">OUTPUTS</span></span>

### <span data-ttu-id="50770-162">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="50770-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="50770-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="50770-163">NOTES</span></span>

## <span data-ttu-id="50770-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50770-164">RELATED LINKS</span></span>

[<span data-ttu-id="50770-165">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="50770-165">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="50770-166">Остановить-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="50770-166">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


