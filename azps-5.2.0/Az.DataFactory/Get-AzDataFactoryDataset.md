---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407516"
---
# <span data-ttu-id="82afe-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="82afe-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="82afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82afe-102">SYNOPSIS</span></span>
<span data-ttu-id="82afe-103">Получает сведения об наборе данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="82afe-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="82afe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82afe-104">SYNTAX</span></span>

### <span data-ttu-id="82afe-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82afe-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82afe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="82afe-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82afe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82afe-107">DESCRIPTION</span></span>
<span data-ttu-id="82afe-108">Для получения сведений об наборе данных в фабрике данных Azure можно получить сведения о наборе данных **Get-AzDataFactoryDataset.**</span><span class="sxs-lookup"><span data-stu-id="82afe-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="82afe-109">Если указать имя для наборов данных, этот cmdlet получит сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="82afe-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="82afe-110">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="82afe-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="82afe-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82afe-111">EXAMPLES</span></span>

### <span data-ttu-id="82afe-112">Пример 1. Просмотр сведений обо всех наборах данных</span><span class="sxs-lookup"><span data-stu-id="82afe-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="82afe-113">Эта команда получает сведения обо всех наборах данных в фабрике данных с именем ВикиADF.</span><span class="sxs-lookup"><span data-stu-id="82afe-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="82afe-114">Пример 2. Просмотр сведений об определенном наборе данных</span><span class="sxs-lookup"><span data-stu-id="82afe-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="82afe-115">Эта команда получает сведения о наборе данных DAWikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="82afe-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="82afe-116">Пример 3. Просмотр расположения для определенного наборов данных</span><span class="sxs-lookup"><span data-stu-id="82afe-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="82afe-117">Эта команда получает сведения о наборе данных DAWikipediaClickEvents в фабрике данных WikiADF,  а затем использует стандартную точку для просмотра расположения, связанного с этим набором данных.</span><span class="sxs-lookup"><span data-stu-id="82afe-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="82afe-118">Кроме того, можно назначить переменной результат из cmdlet **Get-AzDataFactoryDataset,** а затем использовать точку для просмотра свойства Location, связанного с объектом наборов данных, который хранится в этой переменной.</span><span class="sxs-lookup"><span data-stu-id="82afe-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="82afe-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82afe-119">PARAMETERS</span></span>

### <span data-ttu-id="82afe-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="82afe-120">-DataFactory</span></span>
<span data-ttu-id="82afe-121">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="82afe-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="82afe-122">Этот cmdlet получает наборы данных, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="82afe-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="82afe-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="82afe-123">-DataFactoryName</span></span>
<span data-ttu-id="82afe-124">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="82afe-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="82afe-125">Этот cmdlet получает наборы данных, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="82afe-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="82afe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82afe-126">-DefaultProfile</span></span>
<span data-ttu-id="82afe-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82afe-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82afe-128">-Name</span><span class="sxs-lookup"><span data-stu-id="82afe-128">-Name</span></span>
<span data-ttu-id="82afe-129">Определяет имя наборов данных, сведения о которых получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82afe-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="82afe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82afe-130">-ResourceGroupName</span></span>
<span data-ttu-id="82afe-131">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="82afe-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="82afe-132">Этот cmdlet получает наборы данных, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="82afe-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="82afe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82afe-133">CommonParameters</span></span>
<span data-ttu-id="82afe-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82afe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82afe-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82afe-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82afe-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82afe-136">INPUTS</span></span>

### <span data-ttu-id="82afe-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="82afe-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="82afe-138">System.String</span><span class="sxs-lookup"><span data-stu-id="82afe-138">System.String</span></span>

## <span data-ttu-id="82afe-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82afe-139">OUTPUTS</span></span>

### <span data-ttu-id="82afe-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="82afe-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="82afe-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82afe-141">NOTES</span></span>
* <span data-ttu-id="82afe-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="82afe-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="82afe-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82afe-143">RELATED LINKS</span></span>

[<span data-ttu-id="82afe-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="82afe-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="82afe-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="82afe-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)

