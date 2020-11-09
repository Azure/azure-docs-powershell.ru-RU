---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314042"
---
# <span data-ttu-id="b3deb-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b3deb-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="b3deb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3deb-102">SYNOPSIS</span></span>
<span data-ttu-id="b3deb-103">Получает сведения о наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="b3deb-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="b3deb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3deb-104">SYNTAX</span></span>

### <span data-ttu-id="b3deb-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3deb-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3deb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b3deb-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3deb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3deb-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3deb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3deb-108">DESCRIPTION</span></span>
<span data-ttu-id="b3deb-109">Командлет Get-AzDataFactoryV2Dataset получает сведения о наборах данных в фабрике данные Azure.</span><span class="sxs-lookup"><span data-stu-id="b3deb-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="b3deb-110">Если вы задаете имя набора данных, этот командлет получает сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="b3deb-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="b3deb-111">Если имя не задано, этот командлет получает сведения обо всех наборах данных в фабрике.</span><span class="sxs-lookup"><span data-stu-id="b3deb-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="b3deb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3deb-112">EXAMPLES</span></span>

### <span data-ttu-id="b3deb-113">Пример 1: получение сведений обо всех наборах данных</span><span class="sxs-lookup"><span data-stu-id="b3deb-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="b3deb-114">Эта команда получает сведения обо всех наборах данных, которые находятся в data Factory с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b3deb-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b3deb-115">Пример 2: получение сведений о конкретном наборе данных</span><span class="sxs-lookup"><span data-stu-id="b3deb-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="b3deb-116">Эта команда получает сведения о наборе данных с именем DAWikipediaClickEvents в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b3deb-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="b3deb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3deb-117">PARAMETERS</span></span>

### <span data-ttu-id="b3deb-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="b3deb-118">-DataFactory</span></span>
<span data-ttu-id="b3deb-119">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="b3deb-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="b3deb-120">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b3deb-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3deb-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b3deb-121">-DataFactoryName</span></span>
<span data-ttu-id="b3deb-122">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="b3deb-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b3deb-123">Этот командлет получает наборы данных, которые принадлежат к фабрике, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b3deb-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3deb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3deb-124">-DefaultProfile</span></span>
<span data-ttu-id="b3deb-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3deb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3deb-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3deb-126">-Name</span></span>
<span data-ttu-id="b3deb-127">Указывает имя набора данных, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b3deb-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="b3deb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3deb-128">-ResourceGroupName</span></span>
<span data-ttu-id="b3deb-129">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b3deb-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b3deb-130">Этот командлет получает наборы данных, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b3deb-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3deb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3deb-131">-ResourceId</span></span>
<span data-ttu-id="b3deb-132">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="b3deb-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b3deb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3deb-133">CommonParameters</span></span>
<span data-ttu-id="b3deb-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3deb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3deb-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3deb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3deb-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3deb-136">INPUTS</span></span>

### <span data-ttu-id="b3deb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b3deb-137">System.String</span></span>

### <span data-ttu-id="b3deb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b3deb-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b3deb-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3deb-139">OUTPUTS</span></span>

### <span data-ttu-id="b3deb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="b3deb-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="b3deb-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3deb-141">NOTES</span></span>
<span data-ttu-id="b3deb-142">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="b3deb-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b3deb-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3deb-143">RELATED LINKS</span></span>

[<span data-ttu-id="b3deb-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b3deb-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="b3deb-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b3deb-145">Remove-AzDataFactoryV2Dataset</span></span>]()