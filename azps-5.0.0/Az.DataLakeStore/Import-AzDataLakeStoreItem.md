---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313322"
---
# <span data-ttu-id="34811-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="34811-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34811-102">SYNOPSIS</span></span>
<span data-ttu-id="34811-103">Передача локального файла или каталога в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34811-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="34811-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34811-104">SYNTAX</span></span>

### <span data-ttu-id="34811-105">NoDiagnosticLogging (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34811-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34811-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="34811-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34811-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34811-107">DESCRIPTION</span></span>
<span data-ttu-id="34811-108">Командлет **Import-AzDataLakeStoreItem** отправляет локальный файл или каталог в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34811-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="34811-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34811-109">EXAMPLES</span></span>

### <span data-ttu-id="34811-110">Пример 1: Отправка файла</span><span class="sxs-lookup"><span data-stu-id="34811-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="34811-111">Эта команда отправляет файл SrcFile.csv и добавляет его в папку MyFiles в Data Lake Store как File.csv с параллелизмом 4.</span><span class="sxs-lookup"><span data-stu-id="34811-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="34811-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34811-112">PARAMETERS</span></span>

### <span data-ttu-id="34811-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="34811-113">-Account</span></span>
<span data-ttu-id="34811-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34811-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-115">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="34811-115">-Concurrency</span></span>
<span data-ttu-id="34811-116">Указывает количество параллельно загружаемых файлов или блоков.</span><span class="sxs-lookup"><span data-stu-id="34811-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="34811-117">Значение по умолчанию будет вычисляться наилучшим объемом работ на основе системных спецификаций.</span><span class="sxs-lookup"><span data-stu-id="34811-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34811-118">-DefaultProfile</span></span>
<span data-ttu-id="34811-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34811-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34811-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="34811-120">-Destination</span></span>
<span data-ttu-id="34811-121">Указывает путь к Data Lake Store, в который нужно добавить файл или папку, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="34811-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="34811-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="34811-123">При необходимости указывает уровень журнала диагностики, который будет использоваться для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="34811-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="34811-124">По умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="34811-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="34811-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="34811-126">Задает путь к журналу диагностики для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="34811-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-127">-Force</span><span class="sxs-lookup"><span data-stu-id="34811-127">-Force</span></span>
<span data-ttu-id="34811-128">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="34811-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="34811-129">-ForceBinary</span></span>
<span data-ttu-id="34811-130">Указывает на то, что копируемые файлы должны быть скопированы без проблем с новым сохранением строк при добавлении.</span><span class="sxs-lookup"><span data-stu-id="34811-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-131">-Path</span><span class="sxs-lookup"><span data-stu-id="34811-131">-Path</span></span>
<span data-ttu-id="34811-132">Указывает локальный путь к файлу или папке для отправки.</span><span class="sxs-lookup"><span data-stu-id="34811-132">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-133">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="34811-133">-Recurse</span></span>
<span data-ttu-id="34811-134">Указывает, что эта операция должна загрузить все элементы во всех вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="34811-134">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-135">-Резюме</span><span class="sxs-lookup"><span data-stu-id="34811-135">-Resume</span></span>
<span data-ttu-id="34811-136">Указывает, что копируемые файл (-ы) являются продолжением предыдущей отправки.</span><span class="sxs-lookup"><span data-stu-id="34811-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="34811-137">Это приведет к тому, что система попытается возобновить работу из последнего файла, который был передан не полностью.</span><span class="sxs-lookup"><span data-stu-id="34811-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34811-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34811-138">-Confirm</span></span>
<span data-ttu-id="34811-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34811-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34811-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34811-140">-WhatIf</span></span>
<span data-ttu-id="34811-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34811-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34811-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34811-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34811-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34811-143">CommonParameters</span></span>
<span data-ttu-id="34811-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34811-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34811-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34811-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34811-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34811-146">INPUTS</span></span>

### <span data-ttu-id="34811-147">System. String</span><span class="sxs-lookup"><span data-stu-id="34811-147">System.String</span></span>

### <span data-ttu-id="34811-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="34811-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="34811-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="34811-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="34811-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="34811-150">System.Int32</span></span>

### <span data-ttu-id="34811-151">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="34811-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="34811-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34811-152">OUTPUTS</span></span>

### <span data-ttu-id="34811-153">System. String</span><span class="sxs-lookup"><span data-stu-id="34811-153">System.String</span></span>

## <span data-ttu-id="34811-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="34811-154">NOTES</span></span>

## <span data-ttu-id="34811-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34811-155">RELATED LINKS</span></span>

[<span data-ttu-id="34811-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="34811-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="34811-158">Присоединиться к AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="34811-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="34811-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="34811-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="34811-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="34811-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)

