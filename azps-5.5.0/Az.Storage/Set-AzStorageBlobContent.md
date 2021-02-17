---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217225"
---
# <span data-ttu-id="a1dbe-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a1dbe-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="a1dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="a1dbe-103">Отправка локального файла в большой BLOB-файл хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="a1dbe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1dbe-104">SYNTAX</span></span>

### <span data-ttu-id="a1dbe-105">SendManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1dbe-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1dbe-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbe-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1dbe-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbe-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1dbe-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1dbe-108">DESCRIPTION</span></span>
<span data-ttu-id="a1dbe-109">Для отправки локального файла в большой большой BLOB-проект хранилища Azure с его использованием передается проектлет **Set-AzStorageBlobContent.**</span><span class="sxs-lookup"><span data-stu-id="a1dbe-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="a1dbe-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1dbe-110">EXAMPLES</span></span>

### <span data-ttu-id="a1dbe-111">Пример 1. Отправка именоваемой файла</span><span class="sxs-lookup"><span data-stu-id="a1dbe-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="a1dbe-112">Эта команда передает файл с именем PlanningData в BLOB-проект с именем Planning2015.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="a1dbe-113">Пример 2. Отправка всех файлов в текущую папку</span><span class="sxs-lookup"><span data-stu-id="a1dbe-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="a1dbe-114">Эта команда использует Windows PowerShell командлет Get-ChildItem для получения всех файлов в текущей папке и во вложенных папках, а затем передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a1dbe-115">**Cmdlet Set-AzStorageBlobContent** передает файлы в контейнер ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="a1dbe-116">Пример 3. Переписать существующий BLOB-бизнес</span><span class="sxs-lookup"><span data-stu-id="a1dbe-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="a1dbe-117">Эта команда получает BLOB-проект с именем Planning2015 в контейнере ContosoUploads с помощью командлета Get-AzStorageBlob, а затем передает его текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="a1dbe-118">Эта команда передает файл с именем ContosoPlanning в качестве плана 2015.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="a1dbe-119">Эта команда не указывает параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="a1dbe-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="a1dbe-120">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="a1dbe-121">Если команда подтверждена, командлет переопишет существующий BLOB-проект.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="a1dbe-122">Пример 4. Отправка файла в контейнер с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="a1dbe-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="a1dbe-123">Эта команда получает контейнер, который начинается со строки ContosoUpload, с помощью командлета **Get-AzStorageContainer,** а затем передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="a1dbe-124">Эта команда передает файл с именем ContosoPlanning в качестве плана 2015.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="a1dbe-125">Пример 5. Отправка файла на страницу BLOB-файла с метаданными и PremiumPageBlobTier в виде P10</span><span class="sxs-lookup"><span data-stu-id="a1dbe-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="a1dbe-126">Первая команда создает таблицу с метаданными для BLOB-$Metadata.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="a1dbe-127">Вторая команда передает файл с именем ContosoPlanning в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="a1dbe-128">Он содержит метаданные, хранимые в $Metadata, и содержит PremiumPageBlobTier как P10.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="a1dbe-129">Пример 6. Отправка файла в BLOB-объект с указанными свойствами LOB-объектов и настройка StandardBlobTier как классного</span><span class="sxs-lookup"><span data-stu-id="a1dbe-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="a1dbe-130">Эта команда передает файл c:\temp\index.html в контейнер contosouploads с указанными свойствами BLOB-объектов и настроит StandardBlobTier как холодный.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="a1dbe-131">Эта команда получает значение ContentType для свойств BLOB-объектов с помощью API [System.Web.MimeMapping]::GetMimeMapping() API.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="a1dbe-132">Пример 7. Отправка файла в большой бизнес-бизнес с областью шифрования</span><span class="sxs-lookup"><span data-stu-id="a1dbe-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="a1dbe-133">Эта команда передает файл в BLOB-файл с областью шифрования.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="a1dbe-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1dbe-134">PARAMETERS</span></span>

### <span data-ttu-id="a1dbe-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1dbe-135">-AsJob</span></span>
<span data-ttu-id="a1dbe-136">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a1dbe-137">-BLOB</span><span class="sxs-lookup"><span data-stu-id="a1dbe-137">-Blob</span></span>
<span data-ttu-id="a1dbe-138">Имя BLOB-части.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="a1dbe-139">Этот cmdlet передает файл в большой BLOB-файл хранилища Azure, указанный этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1dbe-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="a1dbe-140">-BlobType</span></span>
<span data-ttu-id="a1dbe-141">Тип BLOB-ля, который будет добавлен этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="a1dbe-142">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="a1dbe-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1dbe-143">Заблокировать</span><span class="sxs-lookup"><span data-stu-id="a1dbe-143">Block</span></span>
- <span data-ttu-id="a1dbe-144">Страница</span><span class="sxs-lookup"><span data-stu-id="a1dbe-144">Page</span></span>
- <span data-ttu-id="a1dbe-145">Если для вас задана блокировка, то значение по умолчанию — "Блокировать".</span><span class="sxs-lookup"><span data-stu-id="a1dbe-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="a1dbe-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1dbe-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a1dbe-147">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a1dbe-148">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a1dbe-149">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a1dbe-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a1dbe-150">-CloudBlob</span></span>
<span data-ttu-id="a1dbe-151">Указывает объект **CloudBlob.**</span><span class="sxs-lookup"><span data-stu-id="a1dbe-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="a1dbe-152">Чтобы получить объект **CloudBlob,** используйте Get-AzStorageBlob..</span><span class="sxs-lookup"><span data-stu-id="a1dbe-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a1dbe-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a1dbe-153">-CloudBlobContainer</span></span>
<span data-ttu-id="a1dbe-154">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a1dbe-155">Этот cmdlet uploads content to a blob in the container that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="a1dbe-156">Чтобы получить объект **CloudBlobContainer,** используйте Get-AzStorageContainer..</span><span class="sxs-lookup"><span data-stu-id="a1dbe-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a1dbe-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a1dbe-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a1dbe-158">Указывает максимальное число сетевых звонков.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a1dbe-159">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a1dbe-160">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a1dbe-161">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a1dbe-162">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-162">The default value is 10.</span></span>

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

### <span data-ttu-id="a1dbe-163">-Container</span><span class="sxs-lookup"><span data-stu-id="a1dbe-163">-Container</span></span>
<span data-ttu-id="a1dbe-164">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-164">Specifies the name of a container.</span></span>
<span data-ttu-id="a1dbe-165">Этот cmdlet uploads a file to a blob in the container that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1dbe-166">-Контекст</span><span class="sxs-lookup"><span data-stu-id="a1dbe-166">-Context</span></span>
<span data-ttu-id="a1dbe-167">Определяет контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a1dbe-168">Для получения контекста хранилища используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="a1dbe-169">Чтобы использовать контекст хранилища, созданный из токена SAS без разрешения на чтение, необходимо добавить параметр -Force, чтобы пропустить проверку наличия BLOB-приложений.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="a1dbe-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dbe-170">-DefaultProfile</span></span>
<span data-ttu-id="a1dbe-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1dbe-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="a1dbe-172">-EncryptionScope</span></span>
<span data-ttu-id="a1dbe-173">Область шифрования, используемая при создании запросов к BLOB-проекту.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-173">Encryption scope to be used when making requests to the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1dbe-174">-File</span><span class="sxs-lookup"><span data-stu-id="a1dbe-174">-File</span></span>
<span data-ttu-id="a1dbe-175">Путь к локальному файлу для отправки в качестве содержимого BLOB-файла.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="a1dbe-176">-Force</span><span class="sxs-lookup"><span data-stu-id="a1dbe-176">-Force</span></span>
<span data-ttu-id="a1dbe-177">Указывает на то, что этот cmdlet переопишет существующий BLOB-бизнес без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a1dbe-178">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="a1dbe-178">-Metadata</span></span>
<span data-ttu-id="a1dbe-179">Определяет метаданные для добавленного BLOB-контента.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="a1dbe-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="a1dbe-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="a1dbe-181">Уровень BLOB-сайта страницы</span><span class="sxs-lookup"><span data-stu-id="a1dbe-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="a1dbe-182">-Properties</span><span class="sxs-lookup"><span data-stu-id="a1dbe-182">-Properties</span></span>
<span data-ttu-id="a1dbe-183">Определяет свойства загруженного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="a1dbe-184">Поддерживаются такие свойства: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="a1dbe-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1dbe-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a1dbe-186">Для запроса указывается интервал времени, заданный для времени отрезка времени для стороны обслуживания (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a1dbe-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a1dbe-187">Если заданный интервал задан до обработки запроса службой хранилища, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a1dbe-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="a1dbe-188">-StandardBlobTier</span></span>
<span data-ttu-id="a1dbe-189">Заблокировать уровень BLOB-блоков, допустимые значения — "Hot/Cool/Archive".</span><span class="sxs-lookup"><span data-stu-id="a1dbe-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="a1dbe-190">Подробности в https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="a1dbe-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="a1dbe-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1dbe-191">-Confirm</span></span>
<span data-ttu-id="a1dbe-192">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1dbe-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1dbe-193">-WhatIf</span></span>
<span data-ttu-id="a1dbe-194">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1dbe-195">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1dbe-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dbe-196">CommonParameters</span></span>
<span data-ttu-id="a1dbe-197">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1dbe-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dbe-198">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1dbe-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dbe-199">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1dbe-199">INPUTS</span></span>

### <span data-ttu-id="a1dbe-200">System.String</span><span class="sxs-lookup"><span data-stu-id="a1dbe-200">System.String</span></span>

### <span data-ttu-id="a1dbe-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a1dbe-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a1dbe-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a1dbe-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a1dbe-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1dbe-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a1dbe-204">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1dbe-204">OUTPUTS</span></span>

### <span data-ttu-id="a1dbe-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a1dbe-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a1dbe-206">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1dbe-206">NOTES</span></span>

## <span data-ttu-id="a1dbe-207">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1dbe-207">RELATED LINKS</span></span>

[<span data-ttu-id="a1dbe-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a1dbe-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="a1dbe-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a1dbe-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a1dbe-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a1dbe-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
