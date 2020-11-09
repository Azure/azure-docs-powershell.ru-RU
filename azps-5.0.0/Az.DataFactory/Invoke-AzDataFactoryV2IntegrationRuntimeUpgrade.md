---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313973"
---
# <span data-ttu-id="8665c-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="8665c-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="8665c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8665c-102">SYNOPSIS</span></span>
<span data-ttu-id="8665c-103">Обновляет среду интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="8665c-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="8665c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8665c-104">SYNTAX</span></span>

### <span data-ttu-id="8665c-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8665c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8665c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8665c-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8665c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8665c-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8665c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8665c-108">DESCRIPTION</span></span>
<span data-ttu-id="8665c-109">Командлет **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** обновляет саморазмещенную среду интеграции, если доступна новая версия.</span><span class="sxs-lookup"><span data-stu-id="8665c-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="8665c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8665c-110">EXAMPLES</span></span>

### <span data-ttu-id="8665c-111">Пример 1: обновление среды выполнения интеграции с самостоятельным размещением</span><span class="sxs-lookup"><span data-stu-id="8665c-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="8665c-112">Командлет обновляет саморазмещенную среду интеграции с именем Test-SelfHost-IR в фабрике данных "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="8665c-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="8665c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8665c-113">PARAMETERS</span></span>

### <span data-ttu-id="8665c-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8665c-114">-DataFactoryName</span></span>
<span data-ttu-id="8665c-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8665c-115">The data factory name.</span></span>

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

### <span data-ttu-id="8665c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8665c-116">-DefaultProfile</span></span>
<span data-ttu-id="8665c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8665c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8665c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8665c-118">-InputObject</span></span>
<span data-ttu-id="8665c-119">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="8665c-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="8665c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8665c-120">-Name</span></span>
<span data-ttu-id="8665c-121">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8665c-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="8665c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8665c-122">-ResourceGroupName</span></span>
<span data-ttu-id="8665c-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8665c-123">The resource group name.</span></span>

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

### <span data-ttu-id="8665c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8665c-124">-ResourceId</span></span>
<span data-ttu-id="8665c-125">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8665c-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8665c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8665c-126">-Confirm</span></span>
<span data-ttu-id="8665c-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8665c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8665c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8665c-128">-WhatIf</span></span>
<span data-ttu-id="8665c-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8665c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8665c-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8665c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8665c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8665c-131">CommonParameters</span></span>
<span data-ttu-id="8665c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8665c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8665c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8665c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8665c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8665c-134">INPUTS</span></span>

### <span data-ttu-id="8665c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8665c-135">System.String</span></span>

### <span data-ttu-id="8665c-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8665c-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8665c-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8665c-137">OUTPUTS</span></span>

### <span data-ttu-id="8665c-138">System. void</span><span class="sxs-lookup"><span data-stu-id="8665c-138">System.Void</span></span>

## <span data-ttu-id="8665c-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8665c-139">NOTES</span></span>
<span data-ttu-id="8665c-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="8665c-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8665c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8665c-141">RELATED LINKS</span></span>

<span data-ttu-id="8665c-142">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="8665c-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

