---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ae319662cf7b839524bd44524d63a3ba0a15fe20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563632"
---
# <span data-ttu-id="e18da-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e18da-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e18da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e18da-102">SYNOPSIS</span></span>
<span data-ttu-id="e18da-103">Останавливает управляемую выделенную среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e18da-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e18da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e18da-104">SYNTAX</span></span>

### <span data-ttu-id="e18da-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e18da-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e18da-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e18da-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18da-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e18da-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e18da-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e18da-108">DESCRIPTION</span></span>
<span data-ttu-id="e18da-109">Командлет **Stop-AzureRmDataFactoryV2IntegrationRuntime** останавливает управляемую выделенную среду выполнения интеграции в состоянии Started, которая запускается командлетом Start-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="e18da-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="e18da-110">Ресурсы освобождаются, а состояние переносится в "остановлено".</span><span class="sxs-lookup"><span data-stu-id="e18da-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="e18da-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e18da-111">EXAMPLES</span></span>

### <span data-ttu-id="e18da-112">Пример 1: остановка управляемой среды выполнения интеграции, которая находится в состоянии "начато".</span><span class="sxs-lookup"><span data-stu-id="e18da-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="e18da-113">Тест-reserlved-IR среды выполнения управляемой интеграции находится в состоянии starting.</span><span class="sxs-lookup"><span data-stu-id="e18da-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="e18da-114">После выполнения командлета Stop-AzureRmDataFactoryV2IntegrationRuntime ресурсы освобождаются, а состояние переносится в "остановлено".</span><span class="sxs-lookup"><span data-stu-id="e18da-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="e18da-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e18da-115">PARAMETERS</span></span>

### <span data-ttu-id="e18da-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e18da-116">-DataFactoryName</span></span>
<span data-ttu-id="e18da-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e18da-117">The data factory name.</span></span>

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

### <span data-ttu-id="e18da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18da-118">-DefaultProfile</span></span>
<span data-ttu-id="e18da-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e18da-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e18da-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e18da-120">-Force</span></span>
<span data-ttu-id="e18da-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e18da-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e18da-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e18da-122">-InputObject</span></span>
<span data-ttu-id="e18da-123">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="e18da-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="e18da-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e18da-124">-Name</span></span>
<span data-ttu-id="e18da-125">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e18da-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="e18da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18da-126">-ResourceGroupName</span></span>
<span data-ttu-id="e18da-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e18da-127">The resource group name.</span></span>

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

### <span data-ttu-id="e18da-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e18da-128">-ResourceId</span></span>
<span data-ttu-id="e18da-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e18da-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e18da-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e18da-130">-Confirm</span></span>
<span data-ttu-id="e18da-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e18da-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e18da-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18da-132">-WhatIf</span></span>
<span data-ttu-id="e18da-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="e18da-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e18da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18da-134">CommonParameters</span></span>
<span data-ttu-id="e18da-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e18da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18da-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18da-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18da-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e18da-137">INPUTS</span></span>

### <span data-ttu-id="e18da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e18da-138">System.String</span></span>
<span data-ttu-id="e18da-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e18da-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e18da-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e18da-140">OUTPUTS</span></span>

### <span data-ttu-id="e18da-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e18da-141">System.Boolean</span></span>

## <span data-ttu-id="e18da-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e18da-142">NOTES</span></span>
<span data-ttu-id="e18da-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="e18da-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e18da-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e18da-144">RELATED LINKS</span></span>

[<span data-ttu-id="e18da-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e18da-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
