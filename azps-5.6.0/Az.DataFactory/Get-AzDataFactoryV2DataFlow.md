---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 4838ba48d12fa3a4b1fd7d129e63e0a643357a78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975288"
---
# <span data-ttu-id="4dfca-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="4dfca-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="4dfca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dfca-102">SYNOPSIS</span></span>
<span data-ttu-id="4dfca-103">Получает сведения о потоках данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="4dfca-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="4dfca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4dfca-104">SYNTAX</span></span>

### <span data-ttu-id="4dfca-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4dfca-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dfca-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4dfca-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dfca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4dfca-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dfca-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dfca-108">DESCRIPTION</span></span>
<span data-ttu-id="4dfca-109">Этот Get-AzDataFactoryV2DataFlow получает сведения о потоках данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfca-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="4dfca-110">Если задать имя потока данных, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="4dfca-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="4dfca-111">Если имя не указано, этот cmdlet получает сведения обо всех потоках данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="4dfca-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="4dfca-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4dfca-112">EXAMPLES</span></span>
### <span data-ttu-id="4dfca-113">Пример 1. Сведения обо всех потоках данных</span><span class="sxs-lookup"><span data-stu-id="4dfca-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="4dfca-114">Эта команда получает сведения обо всех потоках данных в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4dfca-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="4dfca-115">Пример 2. Просмотр сведений об определенном потоке данных</span><span class="sxs-lookup"><span data-stu-id="4dfca-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="4dfca-116">Эта команда получает сведения о потоке данных "поток1" в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4dfca-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="4dfca-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dfca-117">PARAMETERS</span></span>

### <span data-ttu-id="4dfca-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4dfca-118">-DataFactory</span></span>
<span data-ttu-id="4dfca-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4dfca-119">The data factory object.</span></span>

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

### <span data-ttu-id="4dfca-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4dfca-120">-DataFactoryName</span></span>
<span data-ttu-id="4dfca-121">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4dfca-121">The data factory name.</span></span>

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

### <span data-ttu-id="4dfca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dfca-122">-DefaultProfile</span></span>
<span data-ttu-id="4dfca-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dfca-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4dfca-124">-Name</span></span>
<span data-ttu-id="4dfca-125">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="4dfca-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dfca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dfca-126">-ResourceGroupName</span></span>
<span data-ttu-id="4dfca-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4dfca-127">The resource group name.</span></span>

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

### <span data-ttu-id="4dfca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dfca-128">-ResourceId</span></span>
<span data-ttu-id="4dfca-129">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="4dfca-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4dfca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dfca-130">CommonParameters</span></span>
<span data-ttu-id="4dfca-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dfca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dfca-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dfca-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dfca-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dfca-133">INPUTS</span></span>

### <span data-ttu-id="4dfca-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4dfca-134">System.String</span></span>

### <span data-ttu-id="4dfca-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4dfca-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4dfca-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4dfca-136">OUTPUTS</span></span>

### <span data-ttu-id="4dfca-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="4dfca-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="4dfca-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4dfca-138">NOTES</span></span>
<span data-ttu-id="4dfca-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="4dfca-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4dfca-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dfca-140">RELATED LINKS</span></span>

[<span data-ttu-id="4dfca-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="4dfca-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="4dfca-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="4dfca-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)