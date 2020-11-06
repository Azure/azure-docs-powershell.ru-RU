---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/invoke-azurermdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: 312ef369e6d191dd96f85a293345d8fa155468b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561872"
---
# <span data-ttu-id="96a66-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="96a66-101">Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="96a66-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96a66-102">SYNOPSIS</span></span>
<span data-ttu-id="96a66-103">Обновляет среду интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="96a66-103">Upgrades self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96a66-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96a66-104">SYNTAX</span></span>

### <span data-ttu-id="96a66-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96a66-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96a66-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96a66-106">ByResourceId</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a66-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="96a66-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a66-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96a66-108">DESCRIPTION</span></span>
<span data-ttu-id="96a66-109">Командлет **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** обновляет саморазмещенную среду интеграции, если доступна новая версия.</span><span class="sxs-lookup"><span data-stu-id="96a66-109">The **Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="96a66-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96a66-110">EXAMPLES</span></span>

### <span data-ttu-id="96a66-111">Пример 1: обновление среды выполнения интеграции с самостоятельным размещением</span><span class="sxs-lookup"><span data-stu-id="96a66-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="96a66-112">Командлет обновляет саморазмещенную среду интеграции с именем Test-SelfHost-IR в фабрике данных "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="96a66-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="96a66-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96a66-113">PARAMETERS</span></span>

### <span data-ttu-id="96a66-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="96a66-114">-DataFactoryName</span></span>
<span data-ttu-id="96a66-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="96a66-115">The data factory name.</span></span>

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

### <span data-ttu-id="96a66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a66-116">-DefaultProfile</span></span>
<span data-ttu-id="96a66-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96a66-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a66-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96a66-118">-InputObject</span></span>
<span data-ttu-id="96a66-119">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="96a66-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="96a66-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96a66-120">-Name</span></span>
<span data-ttu-id="96a66-121">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="96a66-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="96a66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a66-122">-ResourceGroupName</span></span>
<span data-ttu-id="96a66-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96a66-123">The resource group name.</span></span>

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

### <span data-ttu-id="96a66-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96a66-124">-ResourceId</span></span>
<span data-ttu-id="96a66-125">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="96a66-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="96a66-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a66-126">-Confirm</span></span>
<span data-ttu-id="96a66-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96a66-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a66-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a66-128">-WhatIf</span></span>
<span data-ttu-id="96a66-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96a66-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96a66-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96a66-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a66-131">CommonParameters</span></span>
<span data-ttu-id="96a66-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96a66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a66-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a66-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a66-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96a66-134">INPUTS</span></span>

### <span data-ttu-id="96a66-135">System. String</span><span class="sxs-lookup"><span data-stu-id="96a66-135">System.String</span></span>
<span data-ttu-id="96a66-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="96a66-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="96a66-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96a66-137">OUTPUTS</span></span>

### <span data-ttu-id="96a66-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="96a66-138">System.Object</span></span>

## <span data-ttu-id="96a66-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="96a66-139">NOTES</span></span>
<span data-ttu-id="96a66-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="96a66-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="96a66-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96a66-141">RELATED LINKS</span></span>

<span data-ttu-id="96a66-142">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="96a66-142">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

