---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 4f29cf8075160e44fb50d838094ef52f9611e0b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720319"
---
# <span data-ttu-id="6f513-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6f513-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="6f513-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f513-102">SYNOPSIS</span></span>
<span data-ttu-id="6f513-103">Передает локальный файл в большой двоичный объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6f513-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="6f513-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f513-104">SYNTAX</span></span>

### <span data-ttu-id="6f513-105">SendManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f513-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f513-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6f513-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f513-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6f513-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f513-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f513-108">DESCRIPTION</span></span>
<span data-ttu-id="6f513-109">Командлет **Set-AzStorageBlobContent** отправляет локальный файл в большой двоичный объект хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6f513-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="6f513-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f513-110">EXAMPLES</span></span>

### <span data-ttu-id="6f513-111">Пример 1: отправка именованного файла</span><span class="sxs-lookup"><span data-stu-id="6f513-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="6f513-112">Эта команда отправляет файл с именем PlanningData в большой двоичный объект с именем Planning2015.</span><span class="sxs-lookup"><span data-stu-id="6f513-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="6f513-113">Пример 2: отправка всех файлов в текущей папке</span><span class="sxs-lookup"><span data-stu-id="6f513-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="6f513-114">Эта команда использует основной командлет Windows PowerShell, Get-ChildItem для получения всех файлов в текущей папке и во вложенных папках, а затем передает их в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6f513-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6f513-115">Командлет **Set-AzStorageBlobContent** отправляет файлы в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="6f513-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="6f513-116">Пример 3: перезаписать существующий большой двоичный объект</span><span class="sxs-lookup"><span data-stu-id="6f513-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="6f513-117">Эта команда получает большой двоичный объект с именем Planning2015 в контейнере ContosoUploads с помощью командлета Get-AzStorageBlob и передает этот BLOB-объект в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="6f513-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="6f513-118">Команда отправляет файл с именем ContosoPlanning как Planning2015.</span><span class="sxs-lookup"><span data-stu-id="6f513-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="6f513-119">Эта команда не задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="6f513-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="6f513-120">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6f513-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="6f513-121">Если вы подтвердите команду, командлет перезапишет существующий большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="6f513-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="6f513-122">Пример 4: передача файла в контейнер с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="6f513-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="6f513-123">Эта команда получает контейнер, который начинается со строки ContosoUpload с помощью командлета **Get-AzStorageContainer** , а затем передает этот BLOB-объект в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="6f513-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="6f513-124">Команда отправляет файл с именем ContosoPlanning как Planning2015.</span><span class="sxs-lookup"><span data-stu-id="6f513-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="6f513-125">Пример 5: Добавление файла в большой двоичный объект на страницу с помощью метаданных и PremiumPageBlobTier в качестве P10</span><span class="sxs-lookup"><span data-stu-id="6f513-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="6f513-126">В первой команде создается хэш-таблица, которая содержит метаданные для большого двоичного объекта, и эта хэш-таблица сохраняется в переменной $Metadata.</span><span class="sxs-lookup"><span data-stu-id="6f513-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="6f513-127">Вторая команда отправляет файл с именем ContosoPlanning в контейнер с именем ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="6f513-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="6f513-128">Большой двоичный объект включает метаданные, хранящиеся в $Metadata, и имеет PremiumPageBlobTier в качестве P10.</span><span class="sxs-lookup"><span data-stu-id="6f513-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="6f513-129">Пример 6: передача файла в большой двоичный объект с указанными свойствами BLOB-объектов и установка StandardBlobTier как круто</span><span class="sxs-lookup"><span data-stu-id="6f513-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool
```

<span data-ttu-id="6f513-130">Эта команда передает файл с именем ContosoPlanning в контейнер с именем ContosoUploads с указанными свойствами BLOB-объектов и устанавливает StandardBlobTier как круто.</span><span class="sxs-lookup"><span data-stu-id="6f513-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>

## <span data-ttu-id="6f513-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f513-131">PARAMETERS</span></span>

### <span data-ttu-id="6f513-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f513-132">-AsJob</span></span>
<span data-ttu-id="6f513-133">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6f513-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6f513-134">-BLOB</span><span class="sxs-lookup"><span data-stu-id="6f513-134">-Blob</span></span>
<span data-ttu-id="6f513-135">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f513-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="6f513-136">Этот командлет отправляет файл в большой двоичный объект хранилища Azure, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6f513-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f513-137">-BlobType</span><span class="sxs-lookup"><span data-stu-id="6f513-137">-BlobType</span></span>
<span data-ttu-id="6f513-138">Указывает тип большого двоичного объекта, отправляемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6f513-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="6f513-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f513-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f513-140">Блокирован</span><span class="sxs-lookup"><span data-stu-id="6f513-140">Block</span></span>
- <span data-ttu-id="6f513-141">Страница. значение по умолчанию — Block.</span><span class="sxs-lookup"><span data-stu-id="6f513-141">Page The default value is Block.</span></span>

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

### <span data-ttu-id="6f513-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6f513-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6f513-143">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="6f513-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6f513-144">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="6f513-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6f513-145">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6f513-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6f513-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6f513-146">-CloudBlob</span></span>
<span data-ttu-id="6f513-147">Указывает объект **CloudBlob** .</span><span class="sxs-lookup"><span data-stu-id="6f513-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="6f513-148">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="6f513-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6f513-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6f513-149">-CloudBlobContainer</span></span>
<span data-ttu-id="6f513-150">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6f513-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6f513-151">Этот командлет передает содержимое в большой двоичный объект в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6f513-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="6f513-152">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="6f513-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="6f513-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6f513-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6f513-154">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6f513-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6f513-155">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6f513-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6f513-156">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="6f513-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6f513-157">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="6f513-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6f513-158">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="6f513-158">The default value is 10.</span></span>

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

### <span data-ttu-id="6f513-159">-Container</span><span class="sxs-lookup"><span data-stu-id="6f513-159">-Container</span></span>
<span data-ttu-id="6f513-160">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="6f513-160">Specifies the name of a container.</span></span>
<span data-ttu-id="6f513-161">Этот командлет отправляет файл в большой двоичный объект в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6f513-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f513-162">-Context</span><span class="sxs-lookup"><span data-stu-id="6f513-162">-Context</span></span>
<span data-ttu-id="6f513-163">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6f513-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6f513-164">Чтобы получить контекст хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6f513-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="6f513-165">Для использования контекста хранения, созданного из токена SAS без разрешения на чтение, требуется параметр Add-Force для пропуска проверки существования BLOB.</span><span class="sxs-lookup"><span data-stu-id="6f513-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="6f513-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f513-166">-DefaultProfile</span></span>
<span data-ttu-id="6f513-167">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f513-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f513-168">-Файл</span><span class="sxs-lookup"><span data-stu-id="6f513-168">-File</span></span>
<span data-ttu-id="6f513-169">Указывает путь к локальному файлу для файла, который нужно отправить как содержимое BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="6f513-169">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="6f513-170">-Force</span><span class="sxs-lookup"><span data-stu-id="6f513-170">-Force</span></span>
<span data-ttu-id="6f513-171">Указывает на то, что этот командлет перезапишет существующий BLOB-объект без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6f513-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6f513-172">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6f513-172">-Metadata</span></span>
<span data-ttu-id="6f513-173">Задает метаданные для загруженного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6f513-173">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="6f513-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="6f513-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="6f513-175">Уровень больших двоичных объектов страницы</span><span class="sxs-lookup"><span data-stu-id="6f513-175">Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f513-176">-Свойства</span><span class="sxs-lookup"><span data-stu-id="6f513-176">-Properties</span></span>
<span data-ttu-id="6f513-177">Задает свойства для загруженного BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="6f513-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="6f513-178">Поддерживаются следующие свойства: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="6f513-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="6f513-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6f513-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6f513-180">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="6f513-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6f513-181">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6f513-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6f513-182">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6f513-182">-StandardBlobTier</span></span>
<span data-ttu-id="6f513-183">Блокировать уровень больших двоичных объектов. Допустимые значения: горячий/крутой/архивный.</span><span class="sxs-lookup"><span data-stu-id="6f513-183">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="6f513-184">Подробные сведения https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="6f513-184">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="6f513-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f513-185">-Confirm</span></span>
<span data-ttu-id="6f513-186">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f513-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f513-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f513-187">-WhatIf</span></span>
<span data-ttu-id="6f513-188">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f513-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f513-189">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f513-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f513-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f513-190">CommonParameters</span></span>
<span data-ttu-id="6f513-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f513-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f513-192">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f513-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f513-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f513-193">INPUTS</span></span>

### <span data-ttu-id="6f513-194">System. String</span><span class="sxs-lookup"><span data-stu-id="6f513-194">System.String</span></span>

### <span data-ttu-id="6f513-195">Microsoft. Azure. Storage. BLOB. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6f513-195">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6f513-196">Microsoft. Azure. Storage. BLOB. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6f513-196">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6f513-197">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f513-197">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6f513-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f513-198">OUTPUTS</span></span>

### <span data-ttu-id="6f513-199">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6f513-199">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6f513-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f513-200">NOTES</span></span>

## <span data-ttu-id="6f513-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f513-201">RELATED LINKS</span></span>

[<span data-ttu-id="6f513-202">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6f513-202">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="6f513-203">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6f513-203">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6f513-204">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6f513-204">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
