---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414060"
---
# <span data-ttu-id="7d8b9-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="7d8b9-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="7d8b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8b9-103">Обновляется время самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="7d8b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d8b9-104">SYNTAX</span></span>

### <span data-ttu-id="7d8b9-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d8b9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8b9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8b9-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8b9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7d8b9-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8b9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8b9-108">DESCRIPTION</span></span>
<span data-ttu-id="7d8b9-109">При обновлении новой версии **cmdlet Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** обновляется самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="7d8b9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d8b9-110">EXAMPLES</span></span>

### <span data-ttu-id="7d8b9-111">Пример 1. Обновление времени самостоятельной интеграции</span><span class="sxs-lookup"><span data-stu-id="7d8b9-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="7d8b9-112">При этом будет обновлена самоуправленная интеграция с именем test-selfhost-ir в фабрике данных test-df-eu2.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="7d8b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d8b9-113">PARAMETERS</span></span>

### <span data-ttu-id="7d8b9-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d8b9-114">-DataFactoryName</span></span>
<span data-ttu-id="7d8b9-115">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-115">The data factory name.</span></span>

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

### <span data-ttu-id="7d8b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8b9-116">-DefaultProfile</span></span>
<span data-ttu-id="7d8b9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d8b9-118">-InputObject</span></span>
<span data-ttu-id="7d8b9-119">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="7d8b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7d8b9-120">-Name</span></span>
<span data-ttu-id="7d8b9-121">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="7d8b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d8b9-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-123">The resource group name.</span></span>

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

### <span data-ttu-id="7d8b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8b9-124">-ResourceId</span></span>
<span data-ttu-id="7d8b9-125">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7d8b9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d8b9-126">-Confirm</span></span>
<span data-ttu-id="7d8b9-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8b9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8b9-128">-WhatIf</span></span>
<span data-ttu-id="7d8b9-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8b9-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8b9-131">CommonParameters</span></span>
<span data-ttu-id="7d8b9-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8b9-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8b9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8b9-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d8b9-134">INPUTS</span></span>

### <span data-ttu-id="7d8b9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7d8b9-135">System.String</span></span>

### <span data-ttu-id="7d8b9-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7d8b9-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7d8b9-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d8b9-137">OUTPUTS</span></span>

### <span data-ttu-id="7d8b9-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="7d8b9-138">System.Void</span></span>

## <span data-ttu-id="7d8b9-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d8b9-139">NOTES</span></span>
<span data-ttu-id="7d8b9-140">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="7d8b9-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="7d8b9-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d8b9-141">RELATED LINKS</span></span>

<span data-ttu-id="7d8b9-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="7d8b9-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

