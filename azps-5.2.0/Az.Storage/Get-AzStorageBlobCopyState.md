---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325055"
---
# <span data-ttu-id="0a2fb-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="0a2fb-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="0a2fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2fb-103">Возвращает состояние копии BLOB-части хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="0a2fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a2fb-104">SYNTAX</span></span>

### <span data-ttu-id="0a2fb-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a2fb-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0a2fb-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="0a2fb-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0a2fb-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="0a2fb-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0a2fb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a2fb-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2fb-109">**Cmdlet Get-AzStorageBlobCopyState** получает состояние копии BLOB-части хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="0a2fb-110">Он должен запускаться в BLOB-проекте назначения для копирования.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="0a2fb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a2fb-111">EXAMPLES</span></span>

### <span data-ttu-id="0a2fb-112">Пример 1. Просмотр состояния копии BLOB-части</span><span class="sxs-lookup"><span data-stu-id="0a2fb-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="0a2fb-113">Эта команда получает состояние копии BLOB-части с именем ContosoPlanning2015 в контейнере ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="0a2fb-114">Пример 2. Просмотр состояния копии BLOB-проекта с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="0a2fb-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="0a2fb-115">Эта команда получает BLOB-проект ContosoPlanning2015 в контейнере ContosoUploads с помощью командлета **Get-AzStorageBlob,** а затем передает результат текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0a2fb-116">**Cmdlet Get-AzStorageBlobCopyState** получает состояние копирования этого BLOB-части.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="0a2fb-117">Пример 3. Просмотр состояния копии для BLOB-проекта в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="0a2fb-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="0a2fb-118">Эта команда получает контейнер с именем **Get-AzStorageBlob,** а затем передает результат текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="0a2fb-119">Для BLOB-blob-blob с именем ContosoPlanning2015 в этом контейнере состояние копирования получается у **cmdlet Get-AzStorageContainer.**</span><span class="sxs-lookup"><span data-stu-id="0a2fb-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="0a2fb-120">Пример 4. Запуск копирования и конвейер для получения состояния копии</span><span class="sxs-lookup"><span data-stu-id="0a2fb-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="0a2fb-121">Первая команда начинает копировать BLOB-объект "ContosoPlanning2015" в "ContosoPlanning2015_copy" и выводит объект BLOB-объекта destiantion.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="0a2fb-122">Второй канал команд— объект BLOB-объекта destiantion get-AzStorageBlobCopyState, который получит состояние копирования BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="0a2fb-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a2fb-123">PARAMETERS</span></span>

### <span data-ttu-id="0a2fb-124">-BLOB</span><span class="sxs-lookup"><span data-stu-id="0a2fb-124">-Blob</span></span>
<span data-ttu-id="0a2fb-125">Имя BLOB-части.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="0a2fb-126">Этот cmdlet возвращает состояние операции копирования BLOB-параметров для BLOB-проекта хранилища Azure, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="0a2fb-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a2fb-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0a2fb-128">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0a2fb-129">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0a2fb-130">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0a2fb-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0a2fb-131">-CloudBlob</span></span>
<span data-ttu-id="0a2fb-132">Указывает объект **CloudBlob из** библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="0a2fb-133">Чтобы получить объект **CloudBlob,** воспользуйтесь Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="0a2fb-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2fb-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0a2fb-134">-CloudBlobContainer</span></span>
<span data-ttu-id="0a2fb-135">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="0a2fb-136">Этот cmdlet получает состояние копии BLOB-части в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="0a2fb-137">Чтобы получить объект **CloudBlobContainer,** используйте Get-AzStorageContainer..</span><span class="sxs-lookup"><span data-stu-id="0a2fb-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a2fb-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0a2fb-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0a2fb-139">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0a2fb-140">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0a2fb-141">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0a2fb-142">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0a2fb-143">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-143">The default value is 10.</span></span>

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

### <span data-ttu-id="0a2fb-144">-Container</span><span class="sxs-lookup"><span data-stu-id="0a2fb-144">-Container</span></span>
<span data-ttu-id="0a2fb-145">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-145">Specifies the name of a container.</span></span>
<span data-ttu-id="0a2fb-146">Этот cmdlet получает состояние копирования для BLOB-проекта в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="0a2fb-147">-Контекст</span><span class="sxs-lookup"><span data-stu-id="0a2fb-147">-Context</span></span>
<span data-ttu-id="0a2fb-148">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0a2fb-149">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0a2fb-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2fb-150">-DefaultProfile</span></span>
<span data-ttu-id="0a2fb-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a2fb-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a2fb-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0a2fb-153">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="0a2fb-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0a2fb-154">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0a2fb-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="0a2fb-155">-WaitForComplete</span></span>
<span data-ttu-id="0a2fb-156">Указывает на то, что этот cmdlet ждет завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="0a2fb-157">Если этот параметр не задан, этот cmdlet возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="0a2fb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2fb-158">CommonParameters</span></span>
<span data-ttu-id="0a2fb-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a2fb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2fb-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2fb-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2fb-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a2fb-161">INPUTS</span></span>

### <span data-ttu-id="0a2fb-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="0a2fb-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="0a2fb-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="0a2fb-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="0a2fb-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a2fb-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a2fb-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a2fb-165">OUTPUTS</span></span>

### <span data-ttu-id="0a2fb-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="0a2fb-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="0a2fb-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a2fb-167">NOTES</span></span>

## <span data-ttu-id="0a2fb-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a2fb-168">RELATED LINKS</span></span>

[<span data-ttu-id="0a2fb-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a2fb-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="0a2fb-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a2fb-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


