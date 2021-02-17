---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232881"
---
# <span data-ttu-id="da805-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="da805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da805-102">SYNOPSIS</span></span>
<span data-ttu-id="da805-103">Скачивает файл из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da805-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="da805-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da805-104">SYNTAX</span></span>

### <span data-ttu-id="da805-105">NoDiagnosticLogging (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da805-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da805-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="da805-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da805-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da805-107">DESCRIPTION</span></span>
<span data-ttu-id="da805-108">Для скачивания файла из магазина Data Lake Store с его набережной будет скачиваться **cmdlet Export-AzDataLakeStoreItem.**</span><span class="sxs-lookup"><span data-stu-id="da805-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="da805-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da805-109">EXAMPLES</span></span>

### <span data-ttu-id="da805-110">Пример 1. Скачивание элемента из магазина Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="da805-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="da805-111">Эта команда скачивает файл TestSource.csv из магазина Data Lake Store C:\Test.csv при налике 4.</span><span class="sxs-lookup"><span data-stu-id="da805-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="da805-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da805-112">PARAMETERS</span></span>

### <span data-ttu-id="da805-113">-Account</span><span class="sxs-lookup"><span data-stu-id="da805-113">-Account</span></span>
<span data-ttu-id="da805-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da805-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="da805-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="da805-115">-Concurrency</span></span>
<span data-ttu-id="da805-116">Количество файлов или фрагментов, которые нужно скачать параллельно.</span><span class="sxs-lookup"><span data-stu-id="da805-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="da805-117">Значения по умолчанию вычисляются наилучшим образом на основе спецификаций системы.</span><span class="sxs-lookup"><span data-stu-id="da805-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="da805-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da805-118">-DefaultProfile</span></span>
<span data-ttu-id="da805-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da805-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da805-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="da805-120">-Destination</span></span>
<span data-ttu-id="da805-121">Путь к локальному файлу, в который нужно скачать файл.</span><span class="sxs-lookup"><span data-stu-id="da805-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da805-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="da805-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="da805-123">При желании указывает уровень журнала диагностики, который нужно использовать для записи событий во время импорта файла или папки.</span><span class="sxs-lookup"><span data-stu-id="da805-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="da805-124">Значение по умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="da805-124">Default is Error.</span></span>

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

### <span data-ttu-id="da805-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="da805-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="da805-126">Путь к журналу диагностики для записи событий во время импорта файла или папки.</span><span class="sxs-lookup"><span data-stu-id="da805-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="da805-127">-Force</span><span class="sxs-lookup"><span data-stu-id="da805-127">-Force</span></span>
<span data-ttu-id="da805-128">Указывает на то, что данной операцией можно переписать файл назначения, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="da805-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da805-129">-Path</span><span class="sxs-lookup"><span data-stu-id="da805-129">-Path</span></span>
<span data-ttu-id="da805-130">Путь к элементу, который нужно скачать из магазина Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="da805-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da805-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="da805-131">-Recurse</span></span>
<span data-ttu-id="da805-132">Указывает на рекурсивную загрузку папки.</span><span class="sxs-lookup"><span data-stu-id="da805-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="da805-133">-Resume</span><span class="sxs-lookup"><span data-stu-id="da805-133">-Resume</span></span>
<span data-ttu-id="da805-134">Указывает на то, что копированные файлы являются продолжением предыдущей загрузки.</span><span class="sxs-lookup"><span data-stu-id="da805-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="da805-135">Это приведет к попытке возобновления работы системы из файла, который был загружен не полностью.</span><span class="sxs-lookup"><span data-stu-id="da805-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="da805-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da805-136">-Confirm</span></span>
<span data-ttu-id="da805-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da805-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da805-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da805-138">-WhatIf</span></span>
<span data-ttu-id="da805-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da805-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da805-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da805-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da805-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da805-141">CommonParameters</span></span>
<span data-ttu-id="da805-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da805-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da805-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da805-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da805-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da805-144">INPUTS</span></span>

### <span data-ttu-id="da805-145">System.String</span><span class="sxs-lookup"><span data-stu-id="da805-145">System.String</span></span>

### <span data-ttu-id="da805-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="da805-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="da805-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="da805-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="da805-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="da805-148">System.Int32</span></span>

### <span data-ttu-id="da805-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="da805-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="da805-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da805-150">OUTPUTS</span></span>

### <span data-ttu-id="da805-151">System.String</span><span class="sxs-lookup"><span data-stu-id="da805-151">System.String</span></span>

## <span data-ttu-id="da805-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da805-152">NOTES</span></span>

## <span data-ttu-id="da805-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da805-153">RELATED LINKS</span></span>

[<span data-ttu-id="da805-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="da805-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="da805-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="da805-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="da805-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="da805-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="da805-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="da805-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


