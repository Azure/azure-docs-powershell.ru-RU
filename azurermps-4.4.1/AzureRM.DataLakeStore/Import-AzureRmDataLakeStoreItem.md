---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733745"
---
# <span data-ttu-id="87654-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="87654-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87654-102">SYNOPSIS</span></span>
<span data-ttu-id="87654-103">Передача локального файла или каталога в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="87654-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87654-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87654-104">SYNTAX</span></span>

### <span data-ttu-id="87654-105">Без диагностического протоколирования (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87654-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87654-106">Включить ведение журнала диагностики</span><span class="sxs-lookup"><span data-stu-id="87654-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87654-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87654-107">DESCRIPTION</span></span>
<span data-ttu-id="87654-108">Командлет **Import-AzureRmDataLakeStoreItem** отправляет локальный файл или каталог в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="87654-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="87654-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87654-109">EXAMPLES</span></span>

### <span data-ttu-id="87654-110">Пример 1: Отправка файла</span><span class="sxs-lookup"><span data-stu-id="87654-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="87654-111">Эта команда отправляет файл SrcFile.csv и добавляет его в папку MyFiles в Data Lake Store как File.csv.</span><span class="sxs-lookup"><span data-stu-id="87654-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="87654-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87654-112">PARAMETERS</span></span>

### <span data-ttu-id="87654-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="87654-113">-Account</span></span>
<span data-ttu-id="87654-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="87654-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="87654-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="87654-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="87654-116">Укажите максимальное количество файлов, которые нужно добавить в параллельный файл для отправки папки.</span><span class="sxs-lookup"><span data-stu-id="87654-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="87654-117">Значением по умолчанию является 5 (5).</span><span class="sxs-lookup"><span data-stu-id="87654-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87654-118">-Destination</span><span class="sxs-lookup"><span data-stu-id="87654-118">-Destination</span></span>
<span data-ttu-id="87654-119">Указывает путь к Data Lake Store, в который нужно добавить файл или папку, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="87654-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="87654-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="87654-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="87654-121">При необходимости указывает уровень журнала диагностики, который будет использоваться для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="87654-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="87654-122">По умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="87654-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87654-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="87654-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="87654-124">Задает путь к журналу диагностики для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="87654-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87654-125">-Force</span><span class="sxs-lookup"><span data-stu-id="87654-125">-Force</span></span>
<span data-ttu-id="87654-126">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="87654-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="87654-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="87654-127">-ForceBinary</span></span>
<span data-ttu-id="87654-128">Указывает на то, что эта операция отправляет файл как двоичный файл.</span><span class="sxs-lookup"><span data-stu-id="87654-128">Indicates that this operation uploads the file as a binary file.</span></span>

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

### <span data-ttu-id="87654-129">-Path</span><span class="sxs-lookup"><span data-stu-id="87654-129">-Path</span></span>
<span data-ttu-id="87654-130">Указывает локальный путь к файлу или папке для отправки.</span><span class="sxs-lookup"><span data-stu-id="87654-130">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="87654-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="87654-131">-PerFileThreadCount</span></span>
<span data-ttu-id="87654-132">Указывает максимальное количество потоков, используемых для одного файла.</span><span class="sxs-lookup"><span data-stu-id="87654-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="87654-133">Значение по умолчанию — 10 (10).</span><span class="sxs-lookup"><span data-stu-id="87654-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87654-134">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="87654-134">-Recurse</span></span>
<span data-ttu-id="87654-135">Указывает, что эта операция должна загрузить все элементы во всех вложенных папках.</span><span class="sxs-lookup"><span data-stu-id="87654-135">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="87654-136">-Резюме</span><span class="sxs-lookup"><span data-stu-id="87654-136">-Resume</span></span>
<span data-ttu-id="87654-137">Указывает на то, что эта операция должна возобновить ранее отмененную или неудачную отправку.</span><span class="sxs-lookup"><span data-stu-id="87654-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

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

### <span data-ttu-id="87654-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87654-138">-Confirm</span></span>
<span data-ttu-id="87654-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87654-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87654-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87654-140">-WhatIf</span></span>
<span data-ttu-id="87654-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87654-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87654-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87654-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87654-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87654-143">-DefaultProfile</span></span>
<span data-ttu-id="87654-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87654-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87654-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87654-145">CommonParameters</span></span>
<span data-ttu-id="87654-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87654-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87654-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87654-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87654-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87654-148">INPUTS</span></span>

## <span data-ttu-id="87654-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87654-149">OUTPUTS</span></span>

### <span data-ttu-id="87654-150">подстрок</span><span class="sxs-lookup"><span data-stu-id="87654-150">string</span></span>
<span data-ttu-id="87654-151">Полный путь в учетной записи Data Lake Store к выгруженному файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="87654-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="87654-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="87654-152">NOTES</span></span>

## <span data-ttu-id="87654-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87654-153">RELATED LINKS</span></span>

[<span data-ttu-id="87654-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="87654-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="87654-156">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="87654-157">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="87654-158">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="87654-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="87654-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="87654-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


