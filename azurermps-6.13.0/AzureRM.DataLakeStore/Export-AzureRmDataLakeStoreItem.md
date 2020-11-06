---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566487"
---
# <span data-ttu-id="d7178-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="d7178-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7178-102">SYNOPSIS</span></span>
<span data-ttu-id="d7178-103">Загрузка файла из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7178-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7178-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7178-104">SYNTAX</span></span>

### <span data-ttu-id="d7178-105">NoDiagnosticLogging (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7178-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7178-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="d7178-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7178-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7178-107">DESCRIPTION</span></span>
<span data-ttu-id="d7178-108">Командлет **Export-AzureRmDataLakeStoreItem** загружает файл из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7178-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="d7178-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7178-109">EXAMPLES</span></span>

### <span data-ttu-id="d7178-110">Пример 1: Загрузка элемента из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d7178-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="d7178-111">Эта команда загружает файл TestSource.csv из Data Lake Store в C:\Test.csv с параллелизмом 4.</span><span class="sxs-lookup"><span data-stu-id="d7178-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="d7178-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7178-112">PARAMETERS</span></span>

### <span data-ttu-id="d7178-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d7178-113">-Account</span></span>
<span data-ttu-id="d7178-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7178-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d7178-115">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="d7178-115">-Concurrency</span></span>
<span data-ttu-id="d7178-116">Указывает количество параллельно загружаемых файлов или блоков.</span><span class="sxs-lookup"><span data-stu-id="d7178-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="d7178-117">Значение по умолчанию будет вычисляться наилучшим объемом работ на основе системных спецификаций.</span><span class="sxs-lookup"><span data-stu-id="d7178-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="d7178-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7178-118">-DefaultProfile</span></span>
<span data-ttu-id="d7178-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7178-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7178-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="d7178-120">-Destination</span></span>
<span data-ttu-id="d7178-121">Указывает локальный путь к файлу, в который нужно скачать файл.</span><span class="sxs-lookup"><span data-stu-id="d7178-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="d7178-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="d7178-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="d7178-123">При необходимости указывает уровень журнала диагностики, который будет использоваться для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="d7178-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="d7178-124">По умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="d7178-124">Default is Error.</span></span>

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

### <span data-ttu-id="d7178-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="d7178-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="d7178-126">Задает путь к журналу диагностики для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="d7178-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="d7178-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d7178-127">-Force</span></span>
<span data-ttu-id="d7178-128">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="d7178-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="d7178-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d7178-129">-Path</span></span>
<span data-ttu-id="d7178-130">Указывает путь к элементу, загружаемому из Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="d7178-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="d7178-131">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="d7178-131">-Recurse</span></span>
<span data-ttu-id="d7178-132">Указывает, что загружаемая папка является рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="d7178-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="d7178-133">-Резюме</span><span class="sxs-lookup"><span data-stu-id="d7178-133">-Resume</span></span>
<span data-ttu-id="d7178-134">Указывает, что копируемые файл (-ы) являются продолжением предыдущей загрузки.</span><span class="sxs-lookup"><span data-stu-id="d7178-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="d7178-135">Это приведет к тому, что система попытается возобновить работу из последнего файла, который был загружен не полностью.</span><span class="sxs-lookup"><span data-stu-id="d7178-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="d7178-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7178-136">-Confirm</span></span>
<span data-ttu-id="d7178-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7178-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7178-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7178-138">-WhatIf</span></span>
<span data-ttu-id="d7178-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7178-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7178-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7178-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7178-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7178-141">CommonParameters</span></span>
<span data-ttu-id="d7178-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7178-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7178-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7178-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7178-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7178-144">INPUTS</span></span>

### <span data-ttu-id="d7178-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d7178-145">System.String</span></span>

### <span data-ttu-id="d7178-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d7178-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d7178-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7178-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d7178-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d7178-148">System.Int32</span></span>

### <span data-ttu-id="d7178-149">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="d7178-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="d7178-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7178-150">OUTPUTS</span></span>

### <span data-ttu-id="d7178-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d7178-151">System.String</span></span>
<span data-ttu-id="d7178-152">Путь к папке, в которую был загружен файл или папка.</span><span class="sxs-lookup"><span data-stu-id="d7178-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="d7178-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7178-153">NOTES</span></span>

## <span data-ttu-id="d7178-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7178-154">RELATED LINKS</span></span>

[<span data-ttu-id="d7178-155">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d7178-156">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d7178-157">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d7178-158">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d7178-159">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d7178-160">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d7178-161">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7178-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


