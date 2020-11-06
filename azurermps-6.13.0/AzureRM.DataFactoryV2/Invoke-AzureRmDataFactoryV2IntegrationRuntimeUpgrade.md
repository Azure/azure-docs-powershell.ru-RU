---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: b83e6604e854260814a949885d26968542e84efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560979"
---
# <span data-ttu-id="0ccc1-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="0ccc1-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="0ccc1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ccc1-102">SYNOPSIS</span></span>
<span data-ttu-id="0ccc1-103">Обновляет среду интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ccc1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ccc1-104">SYNTAX</span></span>

### <span data-ttu-id="0ccc1-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ccc1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ccc1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ccc1-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ccc1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0ccc1-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ccc1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ccc1-108">DESCRIPTION</span></span>
<span data-ttu-id="0ccc1-109">Командлет **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** обновляет саморазмещенную среду интеграции, если доступна новая версия.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="0ccc1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ccc1-110">EXAMPLES</span></span>

### <span data-ttu-id="0ccc1-111">Пример 1: обновление среды выполнения интеграции с самостоятельным размещением</span><span class="sxs-lookup"><span data-stu-id="0ccc1-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="0ccc1-112">Командлет обновляет саморазмещенную среду интеграции с именем Test-SelfHost-IR в фабрике данных "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="0ccc1-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="0ccc1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ccc1-113">PARAMETERS</span></span>

### <span data-ttu-id="0ccc1-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0ccc1-114">-DataFactoryName</span></span>
<span data-ttu-id="0ccc1-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-115">The data factory name.</span></span>

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

### <span data-ttu-id="0ccc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ccc1-116">-DefaultProfile</span></span>
<span data-ttu-id="0ccc1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ccc1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ccc1-118">-InputObject</span></span>
<span data-ttu-id="0ccc1-119">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="0ccc1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ccc1-120">-Name</span></span>
<span data-ttu-id="0ccc1-121">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="0ccc1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ccc1-122">-ResourceGroupName</span></span>
<span data-ttu-id="0ccc1-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-123">The resource group name.</span></span>

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

### <span data-ttu-id="0ccc1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ccc1-124">-ResourceId</span></span>
<span data-ttu-id="0ccc1-125">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0ccc1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ccc1-126">-Confirm</span></span>
<span data-ttu-id="0ccc1-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ccc1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ccc1-128">-WhatIf</span></span>
<span data-ttu-id="0ccc1-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ccc1-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ccc1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccc1-131">CommonParameters</span></span>
<span data-ttu-id="0ccc1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ccc1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccc1-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ccc1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccc1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ccc1-134">INPUTS</span></span>

### <span data-ttu-id="0ccc1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0ccc1-135">System.String</span></span>

### <span data-ttu-id="0ccc1-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0ccc1-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0ccc1-137">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ccc1-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0ccc1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ccc1-138">OUTPUTS</span></span>

### <span data-ttu-id="0ccc1-139">System. void</span><span class="sxs-lookup"><span data-stu-id="0ccc1-139">System.Void</span></span>

## <span data-ttu-id="0ccc1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ccc1-140">NOTES</span></span>
<span data-ttu-id="0ccc1-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="0ccc1-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0ccc1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ccc1-142">RELATED LINKS</span></span>

<span data-ttu-id="0ccc1-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="0ccc1-143">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

