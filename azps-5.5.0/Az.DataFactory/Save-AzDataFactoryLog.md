---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211225"
---
# <span data-ttu-id="7d786-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="7d786-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="7d786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d786-102">SYNOPSIS</span></span>
<span data-ttu-id="7d786-103">Скачивает файлы журнала из обработки Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7d786-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="7d786-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d786-104">SYNTAX</span></span>

### <span data-ttu-id="7d786-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d786-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d786-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7d786-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d786-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d786-107">DESCRIPTION</span></span>
<span data-ttu-id="7d786-108">С **помощью cmdlet Save-AzDataFactoryLog** можно скачивать на локальный жесткий диск файлы журнала, связанные с обработкой проектов Azure HDInsight из проектов Порося или Свина, а также для настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="7d786-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="7d786-109">Сначала запустите Get-AzDataFactoryRun-файл, чтобы получить код действия, которое будет выполниться для среза данных, а затем используйте его для извлечения файлов журнала из хранилища двоичного большого объекта( BLOB-объекта), связанного с кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="7d786-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="7d786-110">Если параметр *DownloadLogs не задан,* можно просто вернуть расположение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="7d786-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="7d786-111">Если задать *параметр DownloadLogs,* не указав выходной каталог *(выходной* параметр), файлы журнала загружаются в папку "Документы" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d786-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="7d786-112">Если вы *указываете DownloadLogs* вместе с выходной папкой *(Output),* файлы журнала загружаются в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="7d786-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="7d786-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d786-113">EXAMPLES</span></span>

### <span data-ttu-id="7d786-114">Пример 1. Сохранение файлов журнала в определенную папку</span><span class="sxs-lookup"><span data-stu-id="7d786-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="7d786-115">Эта команда сохраняет файлы журнала для действия, которое будет выполниться с помощью ИД 841b77c9-d56c-48d1-99a3-8c16c3e77d39, действие принадлежит конвейеру в фабрике данных LogProcessingFactory в группе ресурсов ADF.</span><span class="sxs-lookup"><span data-stu-id="7d786-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="7d786-116">Файлы журнала сохраняются в папку C:\Test.</span><span class="sxs-lookup"><span data-stu-id="7d786-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="7d786-117">Пример 2. Сохранение файлов журнала в папку "Документы" по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d786-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="7d786-118">Эта команда сохраняет файлы журнала в папку "Документы" (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7d786-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="7d786-119">Пример 3. Просмотр расположения файлов журнала</span><span class="sxs-lookup"><span data-stu-id="7d786-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="7d786-120">Эта команда возвращает расположение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="7d786-120">This command returns the location of log files.</span></span>
<span data-ttu-id="7d786-121">Обратите *внимание, что downloadLogs* не указан.</span><span class="sxs-lookup"><span data-stu-id="7d786-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="7d786-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d786-122">PARAMETERS</span></span>

### <span data-ttu-id="7d786-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d786-123">-DataFactory</span></span>
<span data-ttu-id="7d786-124">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="7d786-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d786-125">-DataFactoryName</span></span>
<span data-ttu-id="7d786-126">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7d786-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7d786-127">Этот cmdlet скачивает файлы журнала для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7d786-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d786-128">-DefaultProfile</span></span>
<span data-ttu-id="7d786-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d786-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d786-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="7d786-130">-DownloadLogs</span></span>
<span data-ttu-id="7d786-131">Указывает на то, что этот cmdlet скачивает файлы журнала на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="7d786-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="7d786-132">Если *папка* вывода не указана, файлы сохраняются в папке "Документы" во вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="7d786-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="7d786-133">-Id</span><span class="sxs-lookup"><span data-stu-id="7d786-133">-Id</span></span>
<span data-ttu-id="7d786-134">Определяет ИД действия, запускаемого для среза данных.</span><span class="sxs-lookup"><span data-stu-id="7d786-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="7d786-135">Чтобы получить Get-AzDataFactoryRun, воспользуйтесь этим Get-AzDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="7d786-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="7d786-136">-Output</span><span class="sxs-lookup"><span data-stu-id="7d786-136">-Output</span></span>
<span data-ttu-id="7d786-137">Определяет выходную папку, в которой сохраняются загруженные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="7d786-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d786-138">-ResourceGroupName</span></span>
<span data-ttu-id="7d786-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="7d786-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7d786-140">Этот cmdlet создает фабрику данных, которая принадлежит к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="7d786-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d786-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d786-141">CommonParameters</span></span>
<span data-ttu-id="7d786-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d786-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d786-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d786-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d786-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d786-144">INPUTS</span></span>

### <span data-ttu-id="7d786-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7d786-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7d786-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7d786-146">System.String</span></span>

## <span data-ttu-id="7d786-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d786-147">OUTPUTS</span></span>

### <span data-ttu-id="7d786-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="7d786-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="7d786-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d786-149">NOTES</span></span>
* <span data-ttu-id="7d786-150">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="7d786-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7d786-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d786-151">RELATED LINKS</span></span>

[<span data-ttu-id="7d786-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="7d786-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="7d786-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d786-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="7d786-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d786-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="7d786-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d786-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="7d786-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="7d786-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="7d786-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="7d786-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


