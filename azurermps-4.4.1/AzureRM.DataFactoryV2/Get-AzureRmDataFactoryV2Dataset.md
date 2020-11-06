---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569571"
---
# <span data-ttu-id="22e2d-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="22e2d-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="22e2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="22e2d-103">Получает сведения о наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="22e2d-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22e2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22e2d-104">SYNTAX</span></span>

### <span data-ttu-id="22e2d-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22e2d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="22e2d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="22e2d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="22e2d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22e2d-107">DESCRIPTION</span></span>
<span data-ttu-id="22e2d-108">Командлет Get-AzureRmDataFactoryV2Dataset получает сведения о наборах данных в фабрике данные Azure.</span><span class="sxs-lookup"><span data-stu-id="22e2d-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="22e2d-109">Если вы задаете имя набора данных, этот командлет получает сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="22e2d-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="22e2d-110">Если имя не задано, этот командлет получает сведения обо всех наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="22e2d-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="22e2d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22e2d-111">EXAMPLES</span></span>

### <span data-ttu-id="22e2d-112">Пример 1: получение сведений обо всех наборах данных</span><span class="sxs-lookup"><span data-stu-id="22e2d-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="22e2d-113">Эта команда получает сведения обо всех наборах данных, которые находятся в data Factory с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="22e2d-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="22e2d-114">Пример 2: получение сведений о конкретном наборе данных</span><span class="sxs-lookup"><span data-stu-id="22e2d-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="22e2d-115">Эта команда получает сведения о наборе данных с именем DAWikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="22e2d-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="22e2d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22e2d-116">PARAMETERS</span></span>

### <span data-ttu-id="22e2d-117">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="22e2d-117">-DataFactory</span></span>
<span data-ttu-id="22e2d-118">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="22e2d-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="22e2d-119">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="22e2d-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22e2d-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="22e2d-120">-DataFactoryName</span></span>
<span data-ttu-id="22e2d-121">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="22e2d-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="22e2d-122">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="22e2d-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e2d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22e2d-123">-Name</span></span>
<span data-ttu-id="22e2d-124">Указывает имя набора данных, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="22e2d-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22e2d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e2d-125">-ResourceGroupName</span></span>
<span data-ttu-id="22e2d-126">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="22e2d-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="22e2d-127">Этот командлет получает наборы данных, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="22e2d-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="22e2d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22e2d-128">INPUTS</span></span>

### <span data-ttu-id="22e2d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="22e2d-129">System.String</span></span>
<span data-ttu-id="22e2d-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="22e2d-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="22e2d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22e2d-131">OUTPUTS</span></span>

### <span data-ttu-id="22e2d-132">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="22e2d-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="22e2d-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="22e2d-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="22e2d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="22e2d-134">NOTES</span></span>
<span data-ttu-id="22e2d-135">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="22e2d-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="22e2d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22e2d-136">RELATED LINKS</span></span>
[<span data-ttu-id="22e2d-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="22e2d-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="22e2d-138">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="22e2d-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
