---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314108"
---
# <span data-ttu-id="3a640-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3a640-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="3a640-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a640-102">SYNOPSIS</span></span>
<span data-ttu-id="3a640-103">Получение сведений о наборах данных в фабрике данные Azure.</span><span class="sxs-lookup"><span data-stu-id="3a640-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="3a640-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a640-104">SYNTAX</span></span>

### <span data-ttu-id="3a640-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a640-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a640-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3a640-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a640-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a640-107">DESCRIPTION</span></span>
<span data-ttu-id="3a640-108">Командлет **Get-AzDataFactoryDataset** получает сведения о наборах данных в фабрике данные Azure.</span><span class="sxs-lookup"><span data-stu-id="3a640-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="3a640-109">Если вы задаете имя набора данных, этот командлет получает сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="3a640-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="3a640-110">Если имя не задано, этот командлет получает сведения обо всех наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="3a640-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="3a640-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a640-111">EXAMPLES</span></span>

### <span data-ttu-id="3a640-112">Пример 1: получение сведений обо всех наборах данных</span><span class="sxs-lookup"><span data-stu-id="3a640-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="3a640-113">Эта команда получает сведения обо всех наборах данных, которые находятся в data Factory с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3a640-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="3a640-114">Пример 2: получение сведений о конкретном наборе данных</span><span class="sxs-lookup"><span data-stu-id="3a640-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="3a640-115">Эта команда получает сведения о наборе данных с именем DAWikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3a640-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="3a640-116">Пример 3: получение расположения для определенного набора данных</span><span class="sxs-lookup"><span data-stu-id="3a640-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="3a640-117">Эта команда получает сведения о наборе данных с именем DAWikipediaClickEvents в фабрике данных с именем WikiADF и использует стандартную нотацию для просмотра **местоположения** , связанного с этим набором данных.</span><span class="sxs-lookup"><span data-stu-id="3a640-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="3a640-118">Кроме того, можно назначить результат командлета **Get-AzDataFactoryDataset** переменной, а затем использовать точечную нотацию для просмотра свойства Location, связанного с объектом DataSet, хранящимся в этой переменной.</span><span class="sxs-lookup"><span data-stu-id="3a640-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="3a640-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a640-119">PARAMETERS</span></span>

### <span data-ttu-id="3a640-120">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="3a640-120">-DataFactory</span></span>
<span data-ttu-id="3a640-121">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3a640-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3a640-122">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3a640-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a640-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3a640-123">-DataFactoryName</span></span>
<span data-ttu-id="3a640-124">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3a640-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3a640-125">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3a640-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a640-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a640-126">-DefaultProfile</span></span>
<span data-ttu-id="3a640-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a640-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a640-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a640-128">-Name</span></span>
<span data-ttu-id="3a640-129">Указывает имя набора данных, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="3a640-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a640-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a640-130">-ResourceGroupName</span></span>
<span data-ttu-id="3a640-131">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3a640-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3a640-132">Этот командлет получает наборы данных, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3a640-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a640-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a640-133">CommonParameters</span></span>
<span data-ttu-id="3a640-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a640-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a640-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a640-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a640-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a640-136">INPUTS</span></span>

### <span data-ttu-id="3a640-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3a640-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3a640-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3a640-138">System.String</span></span>

## <span data-ttu-id="3a640-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a640-139">OUTPUTS</span></span>

### <span data-ttu-id="3a640-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3a640-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="3a640-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a640-141">NOTES</span></span>
* <span data-ttu-id="3a640-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="3a640-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3a640-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a640-143">RELATED LINKS</span></span>

[<span data-ttu-id="3a640-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3a640-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="3a640-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3a640-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


