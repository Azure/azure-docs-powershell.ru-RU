---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566640"
---
# <span data-ttu-id="5ee72-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5ee72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ee72-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee72-103">Передача локального файла или каталога в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5ee72-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ee72-104">SYNTAX</span></span>

### <span data-ttu-id="5ee72-105">NoDiagnosticLogging (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ee72-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ee72-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="5ee72-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ee72-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee72-107">DESCRIPTION</span></span>
<span data-ttu-id="5ee72-108">Командлет **Import-AzureRmDataLakeStoreItem** отправляет локальный файл или каталог в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5ee72-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="5ee72-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ee72-109">EXAMPLES</span></span>

### <span data-ttu-id="5ee72-110">Пример 1: Отправка файла</span><span class="sxs-lookup"><span data-stu-id="5ee72-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="5ee72-111">Эта команда отправляет файл SrcFile.csv и добавляет его в папку MyFiles в Data Lake Store как File.csv с параллелизмом 4.</span><span class="sxs-lookup"><span data-stu-id="5ee72-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="5ee72-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ee72-112">PARAMETERS</span></span>

### <span data-ttu-id="5ee72-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="5ee72-113">-Account</span></span>
<span data-ttu-id="5ee72-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5ee72-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-115">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="5ee72-115">-Concurrency</span></span>
<span data-ttu-id="5ee72-116">Указывает количество параллельно загружаемых файлов или блоков.</span><span class="sxs-lookup"><span data-stu-id="5ee72-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="5ee72-117">Значение по умолчанию будет вычисляться наилучшим объемом работ на основе системных спецификаций.</span><span class="sxs-lookup"><span data-stu-id="5ee72-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="5ee72-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="5ee72-119">Указывает максимальное количество файлов, которые нужно добавить параллельно для отправки папки.</span><span class="sxs-lookup"><span data-stu-id="5ee72-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="5ee72-120">По умолчанию будет вычислено для наилучшей работы с учетом размера папки и файла</span><span class="sxs-lookup"><span data-stu-id="5ee72-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee72-121">-DefaultProfile</span></span>
<span data-ttu-id="5ee72-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee72-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-123">-Destination</span><span class="sxs-lookup"><span data-stu-id="5ee72-123">-Destination</span></span>
<span data-ttu-id="5ee72-124">Указывает путь к Data Lake Store, в который нужно добавить файл или папку, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="5ee72-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5ee72-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5ee72-126">При необходимости указывает уровень журнала диагностики, который будет использоваться для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="5ee72-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5ee72-127">По умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="5ee72-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5ee72-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="5ee72-129">Задает путь к журналу диагностики для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="5ee72-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5ee72-130">-Force</span></span>
<span data-ttu-id="5ee72-131">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="5ee72-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="5ee72-132">-ForceBinary</span></span>
<span data-ttu-id="5ee72-133">Указывает на то, что копируемые файлы должны быть скопированы без проблем с новым сохранением строк при добавлении.</span><span class="sxs-lookup"><span data-stu-id="5ee72-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-134">-Path</span><span class="sxs-lookup"><span data-stu-id="5ee72-134">-Path</span></span>
<span data-ttu-id="5ee72-135">Указывает локальный путь к файлу или папке для отправки.</span><span class="sxs-lookup"><span data-stu-id="5ee72-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="5ee72-136">-PerFileThreadCount</span></span>
<span data-ttu-id="5ee72-137">Указывает максимальное количество потоков, используемых для одного файла.</span><span class="sxs-lookup"><span data-stu-id="5ee72-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="5ee72-138">По умолчанию будет вычислено для наилучшей работы с учетом размера папки и файла</span><span class="sxs-lookup"><span data-stu-id="5ee72-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-139">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="5ee72-139">-Recurse</span></span>
<span data-ttu-id="5ee72-140">Указывает, что эта операция должна загрузить все элементы во всех вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="5ee72-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-141">-Резюме</span><span class="sxs-lookup"><span data-stu-id="5ee72-141">-Resume</span></span>
<span data-ttu-id="5ee72-142">Указывает, что копируемые файл (-ы) являются продолжением предыдущей отправки.</span><span class="sxs-lookup"><span data-stu-id="5ee72-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="5ee72-143">Это приведет к тому, что система попытается возобновить работу из последнего файла, который был передан не полностью.</span><span class="sxs-lookup"><span data-stu-id="5ee72-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ee72-144">-Confirm</span></span>
<span data-ttu-id="5ee72-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ee72-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ee72-146">-WhatIf</span></span>
<span data-ttu-id="5ee72-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ee72-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ee72-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ee72-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ee72-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee72-149">CommonParameters</span></span>
<span data-ttu-id="5ee72-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ee72-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee72-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee72-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee72-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ee72-152">INPUTS</span></span>

### <span data-ttu-id="5ee72-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ee72-153">None</span></span>
<span data-ttu-id="5ee72-154">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5ee72-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ee72-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ee72-155">OUTPUTS</span></span>

### <span data-ttu-id="5ee72-156">подстрок</span><span class="sxs-lookup"><span data-stu-id="5ee72-156">string</span></span>
<span data-ttu-id="5ee72-157">Полный путь в учетной записи Data Lake Store к выгруженному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="5ee72-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="5ee72-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ee72-158">NOTES</span></span>

## <span data-ttu-id="5ee72-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ee72-159">RELATED LINKS</span></span>

[<span data-ttu-id="5ee72-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ee72-161">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ee72-162">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ee72-163">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ee72-164">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ee72-165">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5ee72-166">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ee72-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


