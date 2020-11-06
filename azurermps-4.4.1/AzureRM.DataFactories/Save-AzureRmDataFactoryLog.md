---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 8525333f2be148b59053c62fc4d0f95dda8949a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566741"
---
# <span data-ttu-id="68953-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="68953-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="68953-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68953-102">SYNOPSIS</span></span>
<span data-ttu-id="68953-103">Загружает файлы журнала из службы обработки Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="68953-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68953-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68953-104">SYNTAX</span></span>

### <span data-ttu-id="68953-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68953-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68953-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="68953-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68953-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68953-107">DESCRIPTION</span></span>
<span data-ttu-id="68953-108">Командлет **Save-AzureRmDataFactoryLog** загружает файлы журнала, связанные с обработкой Azure HDInsight для проектов свинья или Hive, или для настраиваемых действий на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="68953-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="68953-109">Сначала необходимо выполнить командлет Get-AzureRmDataFactoryRun, чтобы получить идентификатор для действия, выполняемого для среза данных, а затем использовать этот идентификатор для получения файлов журнала из хранилища BLOB-объектов, связанного с кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="68953-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>

<span data-ttu-id="68953-110">Если параметр *DownloadLogs* не указан, командлет просто возвращает расположение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="68953-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>

<span data-ttu-id="68953-111">Если вы укажете *DownloadLogs* без указания выходного каталога (параметр *Output* ), файлы журнала загружаются в папку документы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68953-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>

<span data-ttu-id="68953-112">Если задать *DownloadLogs* и выходную папку ( *Output* ), файлы журнала будут загружены в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="68953-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="68953-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68953-113">EXAMPLES</span></span>

### <span data-ttu-id="68953-114">Пример 1: сохранение файлов журнала в определенной папке</span><span class="sxs-lookup"><span data-stu-id="68953-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="68953-115">Эта команда позволяет сохранить файлы журнала для действия с ИД 841b77c9-d56c-48d1-99a3-8c16c3e77d39, в котором действие относится к конвейеру в фабрике данных с именем LogProcessingFactory в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="68953-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="68953-116">Файлы журнала сохраняются в папке C:\Test.</span><span class="sxs-lookup"><span data-stu-id="68953-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="68953-117">Пример 2: сохранение файлов журнала в папке "документы по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="68953-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="68953-118">Эта команда позволяет сохранить файлы журнала в папке "документы" (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="68953-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="68953-119">Пример 3: получение расположения файлов журнала</span><span class="sxs-lookup"><span data-stu-id="68953-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="68953-120">Эта команда возвращает расположение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="68953-120">This command returns the location of log files.</span></span>
<span data-ttu-id="68953-121">Обратите внимание, что *DownloadLogs* не указан.</span><span class="sxs-lookup"><span data-stu-id="68953-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="68953-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68953-122">PARAMETERS</span></span>

### <span data-ttu-id="68953-123">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="68953-123">-DataFactory</span></span>
<span data-ttu-id="68953-124">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="68953-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="68953-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="68953-125">-DataFactoryName</span></span>
<span data-ttu-id="68953-126">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="68953-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="68953-127">Этот командлет загружает файлы журнала для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="68953-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="68953-128">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="68953-128">-DownloadLogs</span></span>
<span data-ttu-id="68953-129">Указывает на то, что этот командлет загружает файлы журнала на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="68953-129">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="68953-130">Если папка *Ouptut* не указана, файлы сохраняются в папке "документы" во вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="68953-130">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="68953-131">-ID</span><span class="sxs-lookup"><span data-stu-id="68953-131">-Id</span></span>
<span data-ttu-id="68953-132">Указывает идентификатор действия, выполняемого для среза данных.</span><span class="sxs-lookup"><span data-stu-id="68953-132">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="68953-133">Для получения идентификатора используйте командлет Get-AzureRmDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="68953-133">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="68953-134">-Output</span><span class="sxs-lookup"><span data-stu-id="68953-134">-Output</span></span>
<span data-ttu-id="68953-135">Указывает папку выходных данных, в которой сохраняются Скачанные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="68953-135">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="68953-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68953-136">-ResourceGroupName</span></span>
<span data-ttu-id="68953-137">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="68953-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="68953-138">Этот командлет создает фабрику данных, принадлежащую группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="68953-138">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="68953-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68953-139">-DefaultProfile</span></span>
<span data-ttu-id="68953-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68953-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68953-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68953-141">CommonParameters</span></span>
<span data-ttu-id="68953-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68953-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68953-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68953-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68953-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68953-144">INPUTS</span></span>

## <span data-ttu-id="68953-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68953-145">OUTPUTS</span></span>

### <span data-ttu-id="68953-146">Microsoft. Azure. Commands. Factoring. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="68953-146">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="68953-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="68953-147">NOTES</span></span>
* <span data-ttu-id="68953-148">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="68953-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="68953-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68953-149">RELATED LINKS</span></span>

[<span data-ttu-id="68953-150">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="68953-150">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="68953-151">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="68953-151">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="68953-152">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="68953-152">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="68953-153">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="68953-153">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="68953-154">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="68953-154">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="68953-155">Приостановить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="68953-155">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


