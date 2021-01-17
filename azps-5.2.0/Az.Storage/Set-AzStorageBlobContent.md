---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d99bde2839e1b4e91d6299cd47319827a57f4f33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403319"
---
# <span data-ttu-id="ce7cb-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ce7cb-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="ce7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7cb-103">Отправка локального файла в большой объем хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="ce7cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ce7cb-104">SYNTAX</span></span>

### <span data-ttu-id="ce7cb-105">SendManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce7cb-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7cb-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ce7cb-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce7cb-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ce7cb-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce7cb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce7cb-108">DESCRIPTION</span></span>
<span data-ttu-id="ce7cb-109">С его использованием можно отправить локальный файл в большой **BLOB-проект** хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="ce7cb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ce7cb-110">EXAMPLES</span></span>

### <span data-ttu-id="ce7cb-111">Пример 1. Отправка именоваемой файла</span><span class="sxs-lookup"><span data-stu-id="ce7cb-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="ce7cb-112">Эта команда загружает файл с именем PlanningData в BLOB-проект с именем Planning2015.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="ce7cb-113">Пример 2. Отправка всех файлов в текущую папку</span><span class="sxs-lookup"><span data-stu-id="ce7cb-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="ce7cb-114">Эта команда использует Windows PowerShell командлет Get-ChildItem для получения всех файлов в текущей папке и во вложенных папках, а затем передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ce7cb-115">**Cmdlet Set-AzStorageBlobContent** передает файлы в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="ce7cb-116">Пример 3. Переписать существующий BLOB-бизнес</span><span class="sxs-lookup"><span data-stu-id="ce7cb-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="ce7cb-117">Эта команда получает BLOB-проект с именем Planning2015 в контейнере ContosoUploads с помощью командлета Get-AzStorageBlob, а затем передает его текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="ce7cb-118">Эта команда передает файл с именем ContosoPlanning в качестве плана 2015.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="ce7cb-119">Эта команда не указывает параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="ce7cb-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="ce7cb-120">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="ce7cb-121">Если команда подтверждена, командлет переопишет существующий BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="ce7cb-122">Пример 4. Отправка файла в контейнер с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ce7cb-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="ce7cb-123">Эта команда получает контейнер, который начинается со строки ContosoUpload, с помощью командлета **Get-AzStorageContainer,** а затем передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="ce7cb-124">Команда передает файл с именем ContosoPlanning в качестве плана 2015.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="ce7cb-125">Пример 5. Отправка файла на страницу bLOB-файла с метаданными и PremiumPageBlobTier в виде P10</span><span class="sxs-lookup"><span data-stu-id="ce7cb-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="ce7cb-126">Первая команда создает таблицу с метаданными для BLOB-$Metadata.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="ce7cb-127">Вторая команда передает файл с именем ContosoPlanning в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="ce7cb-128">Он содержит метаданные, хранимые в $Metadata, и содержит PremiumPageBlobTier в виде P10.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="ce7cb-129">Пример 6. Отправка файла в BLOB-объект с указанными свойствами LOB-объектов и настройка StandardBlobTier как классного</span><span class="sxs-lookup"><span data-stu-id="ce7cb-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="ce7cb-130">Эта команда передает файл c:\temp\index.html в контейнер с именем contosouploads с указанными свойствами BLOB-объектов и пометить StandardBlobTier как холодный.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="ce7cb-131">Эта команда получает значение ContentType для свойств BLOB-объектов с помощью API [System.Web.MimeMapping]::GetMimeMapping() API.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="ce7cb-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce7cb-132">PARAMETERS</span></span>

### <span data-ttu-id="ce7cb-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce7cb-133">-AsJob</span></span>
<span data-ttu-id="ce7cb-134">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ce7cb-135">-BLOB</span><span class="sxs-lookup"><span data-stu-id="ce7cb-135">-Blob</span></span>
<span data-ttu-id="ce7cb-136">Указывает имя BLOB-части.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="ce7cb-137">Этот cmdlet передает файл в большой BLOB-файл хранилища Azure, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-138">-BlobType</span><span class="sxs-lookup"><span data-stu-id="ce7cb-138">-BlobType</span></span>
<span data-ttu-id="ce7cb-139">Тип BLOB-ля, который будет загружаться этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="ce7cb-140">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="ce7cb-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce7cb-141">Заблокировать</span><span class="sxs-lookup"><span data-stu-id="ce7cb-141">Block</span></span>
- <span data-ttu-id="ce7cb-142">Страница</span><span class="sxs-lookup"><span data-stu-id="ce7cb-142">Page</span></span>
- <span data-ttu-id="ce7cb-143">Если для вас задана блокировка, то значение по умолчанию — "Блокировать".</span><span class="sxs-lookup"><span data-stu-id="ce7cb-143">Append The default value is Block.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ce7cb-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ce7cb-145">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ce7cb-146">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ce7cb-147">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ce7cb-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ce7cb-148">-CloudBlob</span></span>
<span data-ttu-id="ce7cb-149">Указывает объект **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="ce7cb-149">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="ce7cb-150">Чтобы получить объект **CloudBlob,** используйте Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="ce7cb-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="ce7cb-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ce7cb-151">-CloudBlobContainer</span></span>
<span data-ttu-id="ce7cb-152">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="ce7cb-153">Этот cmdlet uploads content to a blob in the container that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-153">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="ce7cb-154">Чтобы получить объект **CloudBlobContainer,** воспользуйтесь Get-AzStorageContainer управления.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="ce7cb-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ce7cb-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ce7cb-156">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ce7cb-157">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ce7cb-158">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ce7cb-159">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ce7cb-160">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-160">The default value is 10.</span></span>

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

### <span data-ttu-id="ce7cb-161">-Container</span><span class="sxs-lookup"><span data-stu-id="ce7cb-161">-Container</span></span>
<span data-ttu-id="ce7cb-162">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-162">Specifies the name of a container.</span></span>
<span data-ttu-id="ce7cb-163">Этот cmdlet uploads a file to a blob in the container that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-163">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-164">-Контекст</span><span class="sxs-lookup"><span data-stu-id="ce7cb-164">-Context</span></span>
<span data-ttu-id="ce7cb-165">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-165">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ce7cb-166">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-166">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="ce7cb-167">Чтобы использовать контекст хранилища, созданный из токена SAS без разрешения на чтение, необходимо добавить параметр -Force, чтобы пропустить проверку наличия BLOB-приложений.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-167">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="ce7cb-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7cb-168">-DefaultProfile</span></span>
<span data-ttu-id="ce7cb-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7cb-170">-File</span><span class="sxs-lookup"><span data-stu-id="ce7cb-170">-File</span></span>
<span data-ttu-id="ce7cb-171">Путь к локальному файлу для отправки в качестве содержимого BLOB-файла.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-171">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-172">-Force</span><span class="sxs-lookup"><span data-stu-id="ce7cb-172">-Force</span></span>
<span data-ttu-id="ce7cb-173">Указывает на то, что этот cmdlet переопишет существующий BLOB-бизнес без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-173">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ce7cb-174">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="ce7cb-174">-Metadata</span></span>
<span data-ttu-id="ce7cb-175">Определяет метаданные для добавленного BLOB-контента.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-175">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-176">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="ce7cb-176">-PremiumPageBlobTier</span></span>
<span data-ttu-id="ce7cb-177">Уровень BLOB-сайта страницы</span><span class="sxs-lookup"><span data-stu-id="ce7cb-177">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-178">-Properties</span><span class="sxs-lookup"><span data-stu-id="ce7cb-178">-Properties</span></span>
<span data-ttu-id="ce7cb-179">Определяет свойства загруженного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-179">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="ce7cb-180">Поддерживаются такие свойства: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-180">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-181">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ce7cb-181">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ce7cb-182">Указывает для запроса интервал времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="ce7cb-182">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ce7cb-183">Если заданный интервал задан до обработки запроса службой службы хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-183">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ce7cb-184">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="ce7cb-184">-StandardBlobTier</span></span>
<span data-ttu-id="ce7cb-185">Заблокировать уровень BLOB-блоков, допустимые значения — "Hot/Cool/Archive".</span><span class="sxs-lookup"><span data-stu-id="ce7cb-185">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="ce7cb-186">Подробности https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="ce7cb-186">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce7cb-187">-Confirm</span></span>
<span data-ttu-id="ce7cb-188">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7cb-189">-WhatIf</span></span>
<span data-ttu-id="ce7cb-190">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce7cb-191">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7cb-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7cb-192">CommonParameters</span></span>
<span data-ttu-id="ce7cb-193">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7cb-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7cb-194">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7cb-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7cb-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce7cb-195">INPUTS</span></span>

### <span data-ttu-id="ce7cb-196">System.String</span><span class="sxs-lookup"><span data-stu-id="ce7cb-196">System.String</span></span>

### <span data-ttu-id="ce7cb-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ce7cb-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ce7cb-198">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ce7cb-198">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ce7cb-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce7cb-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ce7cb-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ce7cb-200">OUTPUTS</span></span>

### <span data-ttu-id="ce7cb-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ce7cb-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ce7cb-202">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ce7cb-202">NOTES</span></span>

## <span data-ttu-id="ce7cb-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce7cb-203">RELATED LINKS</span></span>

[<span data-ttu-id="ce7cb-204">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ce7cb-204">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="ce7cb-205">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ce7cb-205">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ce7cb-206">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ce7cb-206">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
