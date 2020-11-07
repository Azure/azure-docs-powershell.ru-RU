---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8912717f718bff7c669752e5e49c2796ee94b05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735194"
---
# <span data-ttu-id="d76a8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="d76a8-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="d76a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d76a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d76a8-103">Возвращает данные метрик для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d76a8-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d76a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d76a8-104">SYNTAX</span></span>

### <span data-ttu-id="d76a8-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d76a8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="d76a8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d76a8-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
```

### <span data-ttu-id="d76a8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d76a8-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="d76a8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d76a8-108">DESCRIPTION</span></span>
<span data-ttu-id="d76a8-109">Командлет Get-AzureRmDataFactoryV2IntegrationRuntimeMetric получает данные метрик о среде выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="d76a8-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="d76a8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d76a8-110">EXAMPLES</span></span>

### <span data-ttu-id="d76a8-111">Пример 1: получение метрики среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="d76a8-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="d76a8-112">Эта команда отображает данные метрик о среде выполнения интеграции с именем Test-SelfHost-IR в подписке для группы ресурсов с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="d76a8-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="d76a8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d76a8-113">PARAMETERS</span></span>

### <span data-ttu-id="d76a8-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d76a8-114">-DataFactoryName</span></span>
<span data-ttu-id="d76a8-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="d76a8-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d76a8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d76a8-116">-InputObject</span></span>
<span data-ttu-id="d76a8-117">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="d76a8-117">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d76a8-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d76a8-118">-Name</span></span>
<span data-ttu-id="d76a8-119">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="d76a8-119">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d76a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d76a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="d76a8-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d76a8-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d76a8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d76a8-122">-ResourceId</span></span>
<span data-ttu-id="d76a8-123">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="d76a8-123">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d76a8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d76a8-124">INPUTS</span></span>

### <span data-ttu-id="d76a8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d76a8-125">System.String</span></span>
<span data-ttu-id="d76a8-126">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d76a8-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="d76a8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d76a8-127">OUTPUTS</span></span>

### <span data-ttu-id="d76a8-128">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="d76a8-128">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>


## <span data-ttu-id="d76a8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d76a8-129">NOTES</span></span>

## <span data-ttu-id="d76a8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d76a8-130">RELATED LINKS</span></span>
[<span data-ttu-id="d76a8-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d76a8-131">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

