---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242836"
---
# <span data-ttu-id="5dc41-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5dc41-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5dc41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dc41-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc41-103">Останавливает управляемую выделенную среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5dc41-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="5dc41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dc41-104">SYNTAX</span></span>

### <span data-ttu-id="5dc41-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5dc41-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dc41-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5dc41-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dc41-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5dc41-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dc41-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dc41-108">DESCRIPTION</span></span>
<span data-ttu-id="5dc41-109">Командлет **Stop-AzDataFactoryV2IntegrationRuntime** останавливает управляемую выделенную среду выполнения интеграции в состоянии Started, которая запускается командлетом Start-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="5dc41-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="5dc41-110">Ресурсы освобождаются, а состояние переносится в "остановлено".</span><span class="sxs-lookup"><span data-stu-id="5dc41-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="5dc41-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dc41-111">EXAMPLES</span></span>

### <span data-ttu-id="5dc41-112">Пример 1: остановка управляемой среды выполнения интеграции, которая находится в состоянии "начато".</span><span class="sxs-lookup"><span data-stu-id="5dc41-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="5dc41-113">Тест-reserlved-IR среды выполнения управляемой интеграции находится в состоянии starting.</span><span class="sxs-lookup"><span data-stu-id="5dc41-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="5dc41-114">После выполнения командлета Stop-AzDataFactoryV2IntegrationRuntime ресурсы освобождаются, а состояние переносится в "остановлено".</span><span class="sxs-lookup"><span data-stu-id="5dc41-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="5dc41-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dc41-115">PARAMETERS</span></span>

### <span data-ttu-id="5dc41-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5dc41-116">-DataFactoryName</span></span>
<span data-ttu-id="5dc41-117">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5dc41-117">The data factory name.</span></span>

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

### <span data-ttu-id="5dc41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc41-118">-DefaultProfile</span></span>
<span data-ttu-id="5dc41-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dc41-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dc41-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5dc41-120">-Force</span></span>
<span data-ttu-id="5dc41-121">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5dc41-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc41-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dc41-122">-InputObject</span></span>
<span data-ttu-id="5dc41-123">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="5dc41-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="5dc41-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5dc41-124">-Name</span></span>
<span data-ttu-id="5dc41-125">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="5dc41-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="5dc41-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dc41-126">-ResourceGroupName</span></span>
<span data-ttu-id="5dc41-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5dc41-127">The resource group name.</span></span>

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

### <span data-ttu-id="5dc41-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dc41-128">-ResourceId</span></span>
<span data-ttu-id="5dc41-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="5dc41-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5dc41-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5dc41-130">-Confirm</span></span>
<span data-ttu-id="5dc41-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5dc41-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dc41-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dc41-132">-WhatIf</span></span>
<span data-ttu-id="5dc41-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="5dc41-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5dc41-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc41-134">CommonParameters</span></span>
<span data-ttu-id="5dc41-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dc41-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc41-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc41-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc41-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dc41-137">INPUTS</span></span>

### <span data-ttu-id="5dc41-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5dc41-138">System.String</span></span>

### <span data-ttu-id="5dc41-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5dc41-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5dc41-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dc41-140">OUTPUTS</span></span>

### <span data-ttu-id="5dc41-141">System. void</span><span class="sxs-lookup"><span data-stu-id="5dc41-141">System.Void</span></span>

## <span data-ttu-id="5dc41-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dc41-142">NOTES</span></span>
<span data-ttu-id="5dc41-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="5dc41-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5dc41-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dc41-144">RELATED LINKS</span></span>

[<span data-ttu-id="5dc41-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5dc41-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()