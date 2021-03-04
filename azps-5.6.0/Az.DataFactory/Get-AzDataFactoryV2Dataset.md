---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 938b51b6025a420570ad62b4e9ce815fe832c4cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975272"
---
# <span data-ttu-id="8c93f-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8c93f-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="8c93f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c93f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c93f-103">Получает сведения об наборе данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="8c93f-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="8c93f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8c93f-104">SYNTAX</span></span>

### <span data-ttu-id="8c93f-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c93f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c93f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8c93f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c93f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8c93f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c93f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c93f-108">DESCRIPTION</span></span>
<span data-ttu-id="8c93f-109">Этот Get-AzDataFactoryV2Dataset получает сведения об наборе данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8c93f-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="8c93f-110">Если указать имя для наборов данных, этот cmdlet получит сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="8c93f-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="8c93f-111">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="8c93f-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="8c93f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8c93f-112">EXAMPLES</span></span>

### <span data-ttu-id="8c93f-113">Пример 1. Просмотр сведений обо всех наборах данных</span><span class="sxs-lookup"><span data-stu-id="8c93f-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="8c93f-114">Эта команда получает сведения обо всех наборах данных в фабрике данных с именем ВикиADF.</span><span class="sxs-lookup"><span data-stu-id="8c93f-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="8c93f-115">Пример 2. Просмотр сведений об определенном наборе данных</span><span class="sxs-lookup"><span data-stu-id="8c93f-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="8c93f-116">Эта команда получает сведения о наборе данных DAWikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8c93f-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="8c93f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c93f-117">PARAMETERS</span></span>

### <span data-ttu-id="8c93f-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8c93f-118">-DataFactory</span></span>
<span data-ttu-id="8c93f-119">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="8c93f-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="8c93f-120">Этот cmdlet получает наборы данных, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8c93f-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c93f-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8c93f-121">-DataFactoryName</span></span>
<span data-ttu-id="8c93f-122">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8c93f-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8c93f-123">Этот cmdlet получает наборы данных, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8c93f-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c93f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c93f-124">-DefaultProfile</span></span>
<span data-ttu-id="8c93f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c93f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c93f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8c93f-126">-Name</span></span>
<span data-ttu-id="8c93f-127">Определяет имя наборов данных, сведения о которых нужно получить.</span><span class="sxs-lookup"><span data-stu-id="8c93f-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c93f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c93f-128">-ResourceGroupName</span></span>
<span data-ttu-id="8c93f-129">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8c93f-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8c93f-130">Этот cmdlet получает наборы данных, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8c93f-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8c93f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c93f-131">-ResourceId</span></span>
<span data-ttu-id="8c93f-132">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8c93f-132">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c93f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c93f-133">CommonParameters</span></span>
<span data-ttu-id="8c93f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c93f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c93f-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c93f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c93f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c93f-136">INPUTS</span></span>

### <span data-ttu-id="8c93f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8c93f-137">System.String</span></span>

### <span data-ttu-id="8c93f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8c93f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8c93f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8c93f-139">OUTPUTS</span></span>

### <span data-ttu-id="8c93f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="8c93f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="8c93f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8c93f-141">NOTES</span></span>
<span data-ttu-id="8c93f-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="8c93f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8c93f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c93f-143">RELATED LINKS</span></span>

[<span data-ttu-id="8c93f-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8c93f-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="8c93f-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="8c93f-145">Remove-AzDataFactoryV2Dataset</span></span>]()
