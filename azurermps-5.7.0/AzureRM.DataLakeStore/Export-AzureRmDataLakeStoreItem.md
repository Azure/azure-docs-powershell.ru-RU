---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732374"
---
# <span data-ttu-id="fd603-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="fd603-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd603-102">SYNOPSIS</span></span>
<span data-ttu-id="fd603-103">Загрузка файла из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fd603-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd603-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd603-104">SYNTAX</span></span>

### <span data-ttu-id="fd603-105">NoDiagnosticLogging (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd603-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd603-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="fd603-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd603-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd603-107">DESCRIPTION</span></span>
<span data-ttu-id="fd603-108">Командлет **Export-AzureRmDataLakeStoreItem** загружает файл из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fd603-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="fd603-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd603-109">EXAMPLES</span></span>

### <span data-ttu-id="fd603-110">Пример 1: Загрузка элемента из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="fd603-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="fd603-111">Эта команда загружает файл TestSource.csv из Data Lake Store в C:\Test.csv с параллелизмом 4.</span><span class="sxs-lookup"><span data-stu-id="fd603-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="fd603-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd603-112">PARAMETERS</span></span>

### <span data-ttu-id="fd603-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="fd603-113">-Account</span></span>
<span data-ttu-id="fd603-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fd603-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fd603-115">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="fd603-115">-Concurrency</span></span>
<span data-ttu-id="fd603-116">Указывает количество параллельно загружаемых файлов или блоков.</span><span class="sxs-lookup"><span data-stu-id="fd603-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="fd603-117">Значение по умолчанию будет вычисляться наилучшим объемом работ на основе системных спецификаций.</span><span class="sxs-lookup"><span data-stu-id="fd603-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd603-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="fd603-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="fd603-119">Указывает максимальное количество файлов, загружаемых параллельно для загрузки папки.</span><span class="sxs-lookup"><span data-stu-id="fd603-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="fd603-120">По умолчанию будет вычислено для наилучшей работы с учетом размера папки и файла</span><span class="sxs-lookup"><span data-stu-id="fd603-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="fd603-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd603-121">-DefaultProfile</span></span>
<span data-ttu-id="fd603-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd603-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd603-123">-Destination</span><span class="sxs-lookup"><span data-stu-id="fd603-123">-Destination</span></span>
<span data-ttu-id="fd603-124">Указывает локальный путь к файлу, в который нужно скачать файл.</span><span class="sxs-lookup"><span data-stu-id="fd603-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd603-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="fd603-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="fd603-126">При необходимости указывает уровень журнала диагностики, который будет использоваться для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="fd603-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="fd603-127">По умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="fd603-127">Default is Error.</span></span>

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

### <span data-ttu-id="fd603-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="fd603-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="fd603-129">Задает путь к журналу диагностики для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="fd603-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="fd603-130">-Force</span><span class="sxs-lookup"><span data-stu-id="fd603-130">-Force</span></span>
<span data-ttu-id="fd603-131">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="fd603-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd603-132">-Path</span><span class="sxs-lookup"><span data-stu-id="fd603-132">-Path</span></span>
<span data-ttu-id="fd603-133">Указывает путь к элементу, загружаемому из Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="fd603-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd603-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="fd603-134">-PerFileThreadCount</span></span>
<span data-ttu-id="fd603-135">Указывает максимальное количество потоков, используемых для одного файла.</span><span class="sxs-lookup"><span data-stu-id="fd603-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="fd603-136">По умолчанию будет вычислено для наилучшей работы с учетом размера папки и файла</span><span class="sxs-lookup"><span data-stu-id="fd603-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd603-137">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="fd603-137">-Recurse</span></span>
<span data-ttu-id="fd603-138">Указывает, что загружаемая папка является рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="fd603-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="fd603-139">-Резюме</span><span class="sxs-lookup"><span data-stu-id="fd603-139">-Resume</span></span>
<span data-ttu-id="fd603-140">Указывает, что копируемые файл (-ы) являются продолжением предыдущей загрузки.</span><span class="sxs-lookup"><span data-stu-id="fd603-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="fd603-141">Это приведет к тому, что система попытается возобновить работу из последнего файла, который был загружен не полностью.</span><span class="sxs-lookup"><span data-stu-id="fd603-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="fd603-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd603-142">-Confirm</span></span>
<span data-ttu-id="fd603-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd603-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd603-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd603-144">-WhatIf</span></span>
<span data-ttu-id="fd603-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd603-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd603-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd603-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd603-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd603-147">CommonParameters</span></span>
<span data-ttu-id="fd603-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd603-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd603-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd603-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd603-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd603-150">INPUTS</span></span>

### <span data-ttu-id="fd603-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="fd603-151">None</span></span>
<span data-ttu-id="fd603-152">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="fd603-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd603-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd603-153">OUTPUTS</span></span>

### <span data-ttu-id="fd603-154">подстрок</span><span class="sxs-lookup"><span data-stu-id="fd603-154">string</span></span>
<span data-ttu-id="fd603-155">Путь к папке, в которую был загружен файл или папка.</span><span class="sxs-lookup"><span data-stu-id="fd603-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="fd603-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd603-156">NOTES</span></span>

## <span data-ttu-id="fd603-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd603-157">RELATED LINKS</span></span>

[<span data-ttu-id="fd603-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fd603-159">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fd603-160">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fd603-161">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fd603-162">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fd603-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="fd603-164">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd603-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


