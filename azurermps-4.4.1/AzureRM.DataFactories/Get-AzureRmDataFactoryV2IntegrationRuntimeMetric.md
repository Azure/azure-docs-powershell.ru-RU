---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: aba54b47a5d335bb4f6ef1fbbf7bef66fa694aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559912"
---
# <span data-ttu-id="ceff1-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="ceff1-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="ceff1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceff1-102">SYNOPSIS</span></span>
<span data-ttu-id="ceff1-103">Возвращает данные метрик для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ceff1-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceff1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceff1-104">SYNTAX</span></span>

### <span data-ttu-id="ceff1-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ceff1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceff1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ceff1-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceff1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ceff1-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceff1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceff1-108">DESCRIPTION</span></span>
<span data-ttu-id="ceff1-109">Командлет Get-AzureRmDataFactoryV2IntegrationRuntimeMetric получает данные метрик о среде выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="ceff1-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="ceff1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceff1-110">EXAMPLES</span></span>

### <span data-ttu-id="ceff1-111">Пример 1: получение метрики среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="ceff1-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="ceff1-112">Эта команда отображает данные метрик о среде выполнения интеграции с именем Test-SelfHost-IR в подписке для группы ресурсов с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="ceff1-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="ceff1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceff1-113">PARAMETERS</span></span>

### <span data-ttu-id="ceff1-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ceff1-114">-DataFactoryName</span></span>
<span data-ttu-id="ceff1-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ceff1-115">The data factory name.</span></span>

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

### <span data-ttu-id="ceff1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceff1-116">-InputObject</span></span>
<span data-ttu-id="ceff1-117">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="ceff1-117">The integration runtime object.</span></span>

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

### <span data-ttu-id="ceff1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ceff1-118">-Name</span></span>
<span data-ttu-id="ceff1-119">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="ceff1-119">The integration runtime name.</span></span>

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

### <span data-ttu-id="ceff1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceff1-120">-ResourceGroupName</span></span>
<span data-ttu-id="ceff1-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ceff1-121">The resource group name.</span></span>

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

### <span data-ttu-id="ceff1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceff1-122">-ResourceId</span></span>
<span data-ttu-id="ceff1-123">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="ceff1-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ceff1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceff1-124">-DefaultProfile</span></span>
<span data-ttu-id="ceff1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceff1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceff1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceff1-126">CommonParameters</span></span>
<span data-ttu-id="ceff1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceff1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceff1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceff1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceff1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceff1-129">INPUTS</span></span>

### <span data-ttu-id="ceff1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ceff1-130">System.String</span></span>
<span data-ttu-id="ceff1-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ceff1-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ceff1-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceff1-132">OUTPUTS</span></span>

### <span data-ttu-id="ceff1-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="ceff1-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="ceff1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceff1-134">NOTES</span></span>

## <span data-ttu-id="ceff1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceff1-135">RELATED LINKS</span></span>

[<span data-ttu-id="ceff1-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ceff1-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

