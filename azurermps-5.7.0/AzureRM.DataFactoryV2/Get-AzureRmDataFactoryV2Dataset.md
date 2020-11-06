---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 171431e317b9edbafe83f7c0c836f5543fcbd65d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564960"
---
# <span data-ttu-id="bdd2d-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="bdd2d-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="bdd2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdd2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd2d-103">Получает сведения о наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdd2d-104">SYNTAX</span></span>

### <span data-ttu-id="bdd2d-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdd2d-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdd2d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bdd2d-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdd2d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd2d-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd2d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdd2d-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd2d-109">Командлет Get-AzureRmDataFactoryV2Dataset получает сведения о наборах данных в фабрике данные Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="bdd2d-110">Если вы задаете имя набора данных, этот командлет получает сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="bdd2d-111">Если имя не задано, этот командлет получает сведения обо всех наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="bdd2d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdd2d-112">EXAMPLES</span></span>

### <span data-ttu-id="bdd2d-113">Пример 1: получение сведений обо всех наборах данных</span><span class="sxs-lookup"><span data-stu-id="bdd2d-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="bdd2d-114">Эта команда получает сведения обо всех наборах данных, которые находятся в data Factory с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="bdd2d-115">Пример 2: получение сведений о конкретном наборе данных</span><span class="sxs-lookup"><span data-stu-id="bdd2d-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="bdd2d-116">Эта команда получает сведения о наборе данных с именем DAWikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="bdd2d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdd2d-117">PARAMETERS</span></span>

### <span data-ttu-id="bdd2d-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-118">-DataFactory</span></span>
<span data-ttu-id="bdd2d-119">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="bdd2d-120">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="bdd2d-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bdd2d-121">-DataFactoryName</span></span>
<span data-ttu-id="bdd2d-122">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bdd2d-123">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdd2d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd2d-124">-DefaultProfile</span></span>
<span data-ttu-id="bdd2d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd2d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bdd2d-126">-Name</span></span>
<span data-ttu-id="bdd2d-127">Указывает имя набора данных, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd2d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd2d-128">-ResourceGroupName</span></span>
<span data-ttu-id="bdd2d-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bdd2d-130">Этот командлет получает наборы данных, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdd2d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdd2d-131">-ResourceId</span></span>
<span data-ttu-id="bdd2d-132">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-132">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd2d-133">CommonParameters</span></span>
<span data-ttu-id="bdd2d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdd2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd2d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd2d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdd2d-136">INPUTS</span></span>

### <span data-ttu-id="bdd2d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bdd2d-137">System.String</span></span>
<span data-ttu-id="bdd2d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bdd2d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bdd2d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdd2d-139">OUTPUTS</span></span>

### <span data-ttu-id="bdd2d-140">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="bdd2d-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="bdd2d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="bdd2d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="bdd2d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdd2d-142">NOTES</span></span>
<span data-ttu-id="bdd2d-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="bdd2d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bdd2d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdd2d-144">RELATED LINKS</span></span>

[<span data-ttu-id="bdd2d-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="bdd2d-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="bdd2d-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="bdd2d-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
