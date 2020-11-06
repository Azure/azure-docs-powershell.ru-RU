---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567657"
---
# <span data-ttu-id="4a3bc-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4a3bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a3bc-103">Загрузка файла из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a3bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a3bc-104">SYNTAX</span></span>

### <span data-ttu-id="4a3bc-105">Без диагностического протоколирования (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a3bc-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a3bc-106">Включить ведение журнала диагностики</span><span class="sxs-lookup"><span data-stu-id="4a3bc-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a3bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a3bc-107">DESCRIPTION</span></span>
<span data-ttu-id="4a3bc-108">Командлет **Export-AzureRmDataLakeStoreItem** загружает файл из Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="4a3bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a3bc-109">EXAMPLES</span></span>

### <span data-ttu-id="4a3bc-110">Пример 1: Загрузка элемента из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4a3bc-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="4a3bc-111">Эта команда позволяет загрузить файл TestSource.csv из магазина Data Lake Store в C:\Test.csv.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="4a3bc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a3bc-112">PARAMETERS</span></span>

### <span data-ttu-id="4a3bc-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="4a3bc-113">-Account</span></span>
<span data-ttu-id="4a3bc-114">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4a3bc-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="4a3bc-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="4a3bc-116">Задает максимальное количество файлов, загружаемых параллельно для загрузки папки.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="4a3bc-117">Значением по умолчанию является 5 (5).</span><span class="sxs-lookup"><span data-stu-id="4a3bc-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="4a3bc-118">-Destination</span><span class="sxs-lookup"><span data-stu-id="4a3bc-118">-Destination</span></span>
<span data-ttu-id="4a3bc-119">Указывает локальный путь к файлу, в который нужно скачать файл.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="4a3bc-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="4a3bc-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="4a3bc-121">При необходимости указывает уровень журнала диагностики, который будет использоваться для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="4a3bc-122">По умолчанию — ошибка.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-122">Default is Error.</span></span>

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

### <span data-ttu-id="4a3bc-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="4a3bc-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="4a3bc-124">Задает путь к журналу диагностики для записи событий при импорте файла или папки.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="4a3bc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4a3bc-125">-Force</span></span>
<span data-ttu-id="4a3bc-126">Указывает на то, что эта операция может перезаписать конечный файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="4a3bc-127">-Path</span><span class="sxs-lookup"><span data-stu-id="4a3bc-127">-Path</span></span>
<span data-ttu-id="4a3bc-128">Указывает путь к элементу, загружаемому из Data Lake Store, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="4a3bc-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="4a3bc-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="4a3bc-129">-PerFileThreadCount</span></span>
<span data-ttu-id="4a3bc-130">Указывает максимальное количество потоков, используемых для одного файла.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="4a3bc-131">Значение по умолчанию — 10 (10).</span><span class="sxs-lookup"><span data-stu-id="4a3bc-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a3bc-132">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="4a3bc-132">-Recurse</span></span>
<span data-ttu-id="4a3bc-133">Указывает, что загружаемая папка является рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="4a3bc-134">-Резюме</span><span class="sxs-lookup"><span data-stu-id="4a3bc-134">-Resume</span></span>
<span data-ttu-id="4a3bc-135">Указывает, что копируемый файл или файлы являются продолжением предыдущей загрузки.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="4a3bc-136">Загрузка пытается возобновить работу из последнего файла, который не был полностью загружен.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="4a3bc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a3bc-137">-Confirm</span></span>
<span data-ttu-id="4a3bc-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a3bc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a3bc-139">-WhatIf</span></span>
<span data-ttu-id="4a3bc-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a3bc-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a3bc-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a3bc-142">-DefaultProfile</span></span>
<span data-ttu-id="4a3bc-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a3bc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a3bc-144">CommonParameters</span></span>
<span data-ttu-id="4a3bc-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a3bc-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a3bc-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a3bc-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a3bc-147">INPUTS</span></span>

## <span data-ttu-id="4a3bc-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a3bc-148">OUTPUTS</span></span>

### <span data-ttu-id="4a3bc-149">подстрок</span><span class="sxs-lookup"><span data-stu-id="4a3bc-149">string</span></span>
<span data-ttu-id="4a3bc-150">Путь к папке, в которую был загружен файл или папка.</span><span class="sxs-lookup"><span data-stu-id="4a3bc-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="4a3bc-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a3bc-151">NOTES</span></span>

## <span data-ttu-id="4a3bc-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a3bc-152">RELATED LINKS</span></span>

[<span data-ttu-id="4a3bc-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4a3bc-154">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4a3bc-155">Присоединиться к AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4a3bc-156">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4a3bc-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4a3bc-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4a3bc-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4a3bc-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


