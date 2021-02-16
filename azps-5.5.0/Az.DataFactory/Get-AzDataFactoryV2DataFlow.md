---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 7bd25d444a4277e2aa423026be551fab1c5f360e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415161"
---
# <span data-ttu-id="1fb00-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="1fb00-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="1fb00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb00-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb00-103">Получает сведения о потоках данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1fb00-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="1fb00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1fb00-104">SYNTAX</span></span>

### <span data-ttu-id="1fb00-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fb00-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb00-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1fb00-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb00-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb00-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb00-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fb00-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb00-109">Этот Get-AzDataFactoryV2DataFlow получает сведения о потоках данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb00-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="1fb00-110">Если задать имя потока данных, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="1fb00-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="1fb00-111">Если имя не указано, этот cmdlet получает сведения обо всех потоках данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1fb00-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="1fb00-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1fb00-112">EXAMPLES</span></span>
### <span data-ttu-id="1fb00-113">Пример 1. Сведения обо всех потоках данных</span><span class="sxs-lookup"><span data-stu-id="1fb00-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="1fb00-114">Эта команда получает сведения обо всех потоках данных в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1fb00-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1fb00-115">Пример 2. Просмотр сведений об определенном потоке данных</span><span class="sxs-lookup"><span data-stu-id="1fb00-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="1fb00-116">Эта команда получает сведения о потоке данных "Поток1" в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1fb00-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="1fb00-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fb00-117">PARAMETERS</span></span>

### <span data-ttu-id="1fb00-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1fb00-118">-DataFactory</span></span>
<span data-ttu-id="1fb00-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1fb00-119">The data factory object.</span></span>

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

### <span data-ttu-id="1fb00-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1fb00-120">-DataFactoryName</span></span>
<span data-ttu-id="1fb00-121">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1fb00-121">The data factory name.</span></span>

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

### <span data-ttu-id="1fb00-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb00-122">-DefaultProfile</span></span>
<span data-ttu-id="1fb00-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb00-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb00-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1fb00-124">-Name</span></span>
<span data-ttu-id="1fb00-125">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="1fb00-125">The data flow name.</span></span>

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

### <span data-ttu-id="1fb00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb00-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fb00-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fb00-127">The resource group name.</span></span>

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

### <span data-ttu-id="1fb00-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb00-128">-ResourceId</span></span>
<span data-ttu-id="1fb00-129">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb00-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1fb00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb00-130">CommonParameters</span></span>
<span data-ttu-id="1fb00-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb00-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fb00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb00-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fb00-133">INPUTS</span></span>

### <span data-ttu-id="1fb00-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1fb00-134">System.String</span></span>

### <span data-ttu-id="1fb00-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fb00-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1fb00-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1fb00-136">OUTPUTS</span></span>

### <span data-ttu-id="1fb00-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="1fb00-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="1fb00-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1fb00-138">NOTES</span></span>
<span data-ttu-id="1fb00-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="1fb00-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1fb00-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fb00-140">RELATED LINKS</span></span>


