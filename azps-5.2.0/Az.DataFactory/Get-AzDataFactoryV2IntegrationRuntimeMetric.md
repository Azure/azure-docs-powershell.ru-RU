---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393588"
---
# <span data-ttu-id="11461-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="11461-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="11461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11461-102">SYNOPSIS</span></span>
<span data-ttu-id="11461-103">Получает метрические данные для интеграции с runtime.</span><span class="sxs-lookup"><span data-stu-id="11461-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="11461-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11461-104">SYNTAX</span></span>

### <span data-ttu-id="11461-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11461-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11461-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="11461-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11461-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="11461-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11461-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11461-108">DESCRIPTION</span></span>
<span data-ttu-id="11461-109">Новый Get-AzDataFactoryV2IntegrationRuntimeMetric получает метрические данные об интеграции с заводом данных.</span><span class="sxs-lookup"><span data-stu-id="11461-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="11461-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11461-110">EXAMPLES</span></span>

### <span data-ttu-id="11461-111">Пример 1. Метрическая система интеграции со временем запуска</span><span class="sxs-lookup"><span data-stu-id="11461-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="11461-112">Эта команда отображает метрические данные об интеграции runtime "test-selfhost-ir" в подписке для группы ресурсов "rg-test-dfv2" и фабрики данных "test-df-eu2".</span><span class="sxs-lookup"><span data-stu-id="11461-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="11461-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11461-113">PARAMETERS</span></span>

### <span data-ttu-id="11461-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="11461-114">-DataFactoryName</span></span>
<span data-ttu-id="11461-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="11461-115">The data factory name.</span></span>

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

### <span data-ttu-id="11461-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11461-116">-DefaultProfile</span></span>
<span data-ttu-id="11461-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11461-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11461-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11461-118">-InputObject</span></span>
<span data-ttu-id="11461-119">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="11461-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="11461-120">-Name</span><span class="sxs-lookup"><span data-stu-id="11461-120">-Name</span></span>
<span data-ttu-id="11461-121">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="11461-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="11461-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11461-122">-ResourceGroupName</span></span>
<span data-ttu-id="11461-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11461-123">The resource group name.</span></span>

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

### <span data-ttu-id="11461-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11461-124">-ResourceId</span></span>
<span data-ttu-id="11461-125">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="11461-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="11461-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11461-126">CommonParameters</span></span>
<span data-ttu-id="11461-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11461-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11461-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11461-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11461-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11461-129">INPUTS</span></span>

### <span data-ttu-id="11461-130">System.String</span><span class="sxs-lookup"><span data-stu-id="11461-130">System.String</span></span>

### <span data-ttu-id="11461-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="11461-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="11461-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11461-132">OUTPUTS</span></span>

### <span data-ttu-id="11461-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="11461-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="11461-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11461-134">NOTES</span></span>

## <span data-ttu-id="11461-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11461-135">RELATED LINKS</span></span>

[<span data-ttu-id="11461-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="11461-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

