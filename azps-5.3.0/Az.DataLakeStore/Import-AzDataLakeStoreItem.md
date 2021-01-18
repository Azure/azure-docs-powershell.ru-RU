---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504582"
---
# <span data-ttu-id="53491-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="53491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53491-102">SYNOPSIS</span></span>
<span data-ttu-id="53491-103">Отправка локального файла или каталога в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53491-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="53491-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53491-104">SYNTAX</span></span>

### <span data-ttu-id="53491-105">NoDiagnosticLogging (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53491-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53491-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="53491-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53491-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53491-107">DESCRIPTION</span></span>
<span data-ttu-id="53491-108">При **этом локальный** файл или каталог загружается в хранилище Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53491-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="53491-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53491-109">EXAMPLES</span></span>

### <span data-ttu-id="53491-110">Пример 1. Отправка файла</span><span class="sxs-lookup"><span data-stu-id="53491-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="53491-111">Эта команда добавляет файл SrcFile.csv и добавляет его в папку MyFiles в магазине Data Lake Store как папку File.csv, причем ее размер составляет 4.</span><span class="sxs-lookup"><span data-stu-id="53491-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="53491-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53491-112">PARAMETERS</span></span>

### <span data-ttu-id="53491-113">-Account</span><span class="sxs-lookup"><span data-stu-id="53491-113">-Account</span></span>
<span data-ttu-id="53491-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53491-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="53491-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="53491-115">-Concurrency</span></span>
<span data-ttu-id="53491-116">Указывает количество файлов или фрагментов, которые нужно добавить параллельно.</span><span class="sxs-lookup"><span data-stu-id="53491-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="53491-117">Значения по умолчанию вычисляются наилучшим образом на основе спецификаций системы.</span><span class="sxs-lookup"><span data-stu-id="53491-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="53491-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53491-118">-DefaultProfile</span></span>
<span data-ttu-id="53491-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53491-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53491-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="53491-120">-Destination</span></span>
<span data-ttu-id="53491-121">Путь к магазину данных для передачи файла или папки, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="53491-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="53491-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="53491-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="53491-123">При желании указывает уровень журнала диагностики, который нужно использовать для записи событий во время импорта файла или папки.</span><span class="sxs-lookup"><span data-stu-id="53491-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="53491-124">Значение по умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="53491-124">Default is Error.</span></span>

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

### <span data-ttu-id="53491-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="53491-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="53491-126">Путь к журналу диагностики для записи событий во время импорта файла или папки.</span><span class="sxs-lookup"><span data-stu-id="53491-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="53491-127">-Force</span><span class="sxs-lookup"><span data-stu-id="53491-127">-Force</span></span>
<span data-ttu-id="53491-128">Указывает на то, что данной операцией можно переписать файл назначения, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="53491-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="53491-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="53491-129">-ForceBinary</span></span>
<span data-ttu-id="53491-130">Указывает на то, что копированные файлы следует копировать, не опасаяся сохранения новой строки во всех приложениях.</span><span class="sxs-lookup"><span data-stu-id="53491-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="53491-131">-Path</span><span class="sxs-lookup"><span data-stu-id="53491-131">-Path</span></span>
<span data-ttu-id="53491-132">Указывает локальный путь к файлу или папке, которые нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="53491-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="53491-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="53491-133">-Recurse</span></span>
<span data-ttu-id="53491-134">Указывает на то, что в ходе этой операции должны быть загружены все элементы из всех вложенных в нее вложенных пунктов.</span><span class="sxs-lookup"><span data-stu-id="53491-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="53491-135">-Resume</span><span class="sxs-lookup"><span data-stu-id="53491-135">-Resume</span></span>
<span data-ttu-id="53491-136">Указывает на то, что копированные файлы являются продолжением предыдущей отправки.</span><span class="sxs-lookup"><span data-stu-id="53491-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="53491-137">Это приведет к попытке возобновления работы системы из файла, который был загружен не полностью.</span><span class="sxs-lookup"><span data-stu-id="53491-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="53491-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53491-138">-Confirm</span></span>
<span data-ttu-id="53491-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53491-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53491-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53491-140">-WhatIf</span></span>
<span data-ttu-id="53491-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53491-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53491-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53491-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53491-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53491-143">CommonParameters</span></span>
<span data-ttu-id="53491-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53491-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53491-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53491-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53491-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53491-146">INPUTS</span></span>

### <span data-ttu-id="53491-147">System.String</span><span class="sxs-lookup"><span data-stu-id="53491-147">System.String</span></span>

### <span data-ttu-id="53491-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="53491-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="53491-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53491-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="53491-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="53491-150">System.Int32</span></span>

### <span data-ttu-id="53491-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="53491-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="53491-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53491-152">OUTPUTS</span></span>

### <span data-ttu-id="53491-153">System.String</span><span class="sxs-lookup"><span data-stu-id="53491-153">System.String</span></span>

## <span data-ttu-id="53491-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53491-154">NOTES</span></span>

## <span data-ttu-id="53491-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53491-155">RELATED LINKS</span></span>

[<span data-ttu-id="53491-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="53491-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="53491-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="53491-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="53491-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="53491-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="53491-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="53491-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


