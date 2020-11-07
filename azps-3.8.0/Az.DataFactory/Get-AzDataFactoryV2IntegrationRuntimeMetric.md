---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912876"
---
# <span data-ttu-id="125b3-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="125b3-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="125b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="125b3-102">SYNOPSIS</span></span>
<span data-ttu-id="125b3-103">Возвращает данные метрик для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="125b3-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="125b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="125b3-104">SYNTAX</span></span>

### <span data-ttu-id="125b3-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="125b3-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="125b3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="125b3-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="125b3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="125b3-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="125b3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="125b3-108">DESCRIPTION</span></span>
<span data-ttu-id="125b3-109">Командлет Get-AzDataFactoryV2IntegrationRuntimeMetric получает данные метрик о среде выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="125b3-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="125b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="125b3-110">EXAMPLES</span></span>

### <span data-ttu-id="125b3-111">Пример 1: получение метрики среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="125b3-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="125b3-112">Эта команда отображает данные метрик о среде выполнения интеграции с именем Test-SelfHost-IR в подписке для группы ресурсов с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="125b3-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="125b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="125b3-113">PARAMETERS</span></span>

### <span data-ttu-id="125b3-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="125b3-114">-DataFactoryName</span></span>
<span data-ttu-id="125b3-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="125b3-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="125b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125b3-116">-DefaultProfile</span></span>
<span data-ttu-id="125b3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="125b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="125b3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="125b3-118">-InputObject</span></span>
<span data-ttu-id="125b3-119">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="125b3-119">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="125b3-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="125b3-120">-Name</span></span>
<span data-ttu-id="125b3-121">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="125b3-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="125b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="125b3-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="125b3-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="125b3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="125b3-124">-ResourceId</span></span>
<span data-ttu-id="125b3-125">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="125b3-125">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="125b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125b3-126">CommonParameters</span></span>
<span data-ttu-id="125b3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="125b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125b3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="125b3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125b3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="125b3-129">INPUTS</span></span>

### <span data-ttu-id="125b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="125b3-130">System.String</span></span>

### <span data-ttu-id="125b3-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="125b3-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="125b3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="125b3-132">OUTPUTS</span></span>

### <span data-ttu-id="125b3-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="125b3-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="125b3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="125b3-134">NOTES</span></span>

## <span data-ttu-id="125b3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="125b3-135">RELATED LINKS</span></span>

[<span data-ttu-id="125b3-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="125b3-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

