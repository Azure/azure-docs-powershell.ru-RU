---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079714"
---
# <span data-ttu-id="c9829-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="c9829-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="c9829-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9829-102">SYNOPSIS</span></span>
<span data-ttu-id="c9829-103">Возвращает сведения о потоках данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="c9829-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="c9829-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9829-104">SYNTAX</span></span>

### <span data-ttu-id="c9829-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9829-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9829-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c9829-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9829-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9829-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9829-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9829-108">DESCRIPTION</span></span>
<span data-ttu-id="c9829-109">Командлет Get-AzDataFactoryV2DataFlow получает сведения о потоках данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="c9829-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="c9829-110">Если вы задаете имя потока данных, этот командлет получает сведения об этом потоке данных.</span><span class="sxs-lookup"><span data-stu-id="c9829-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="c9829-111">Если имя не задано, этот командлет получает сведения обо всех потоках данных в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="c9829-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="c9829-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9829-112">EXAMPLES</span></span>
### <span data-ttu-id="c9829-113">Пример 1: получение сведений обо всех потоках данных</span><span class="sxs-lookup"><span data-stu-id="c9829-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="c9829-114">Эта команда получает сведения обо всех потоках данных в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c9829-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c9829-115">Пример 2: получение сведений об определенном потоке данных</span><span class="sxs-lookup"><span data-stu-id="c9829-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="c9829-116">Эта команда получает сведения о потоке данных с именем dataflow1 в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c9829-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="c9829-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9829-117">PARAMETERS</span></span>

### <span data-ttu-id="c9829-118">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="c9829-118">-DataFactory</span></span>
<span data-ttu-id="c9829-119">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c9829-119">The data factory object.</span></span>

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

### <span data-ttu-id="c9829-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c9829-120">-DataFactoryName</span></span>
<span data-ttu-id="c9829-121">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c9829-121">The data factory name.</span></span>

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

### <span data-ttu-id="c9829-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9829-122">-DefaultProfile</span></span>
<span data-ttu-id="c9829-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9829-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9829-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9829-124">-Name</span></span>
<span data-ttu-id="c9829-125">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="c9829-125">The data flow name.</span></span>

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

### <span data-ttu-id="c9829-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9829-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9829-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9829-127">The resource group name.</span></span>

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

### <span data-ttu-id="c9829-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9829-128">-ResourceId</span></span>
<span data-ttu-id="c9829-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="c9829-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c9829-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9829-130">CommonParameters</span></span>
<span data-ttu-id="c9829-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9829-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9829-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9829-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9829-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9829-133">INPUTS</span></span>

### <span data-ttu-id="c9829-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c9829-134">System.String</span></span>

### <span data-ttu-id="c9829-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c9829-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="c9829-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9829-136">OUTPUTS</span></span>

### <span data-ttu-id="c9829-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span><span class="sxs-lookup"><span data-stu-id="c9829-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="c9829-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9829-138">NOTES</span></span>
<span data-ttu-id="c9829-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="c9829-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c9829-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9829-140">RELATED LINKS</span></span>

[<span data-ttu-id="c9829-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="c9829-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="c9829-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="c9829-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)