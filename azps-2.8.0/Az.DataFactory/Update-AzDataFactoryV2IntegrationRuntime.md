---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: d2177e2ca7705f579921b9e2eb9fc64ab0e0c33a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721411"
---
# <span data-ttu-id="e8b2a-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e8b2a-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e8b2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b2a-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="e8b2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8b2a-104">SYNTAX</span></span>

### <span data-ttu-id="e8b2a-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8b2a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b2a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b2a-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b2a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e8b2a-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8b2a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b2a-108">DESCRIPTION</span></span>
<span data-ttu-id="e8b2a-109">Командлет **Update-AzDataFactoryV2IntegrationRuntime** обновляет свойства среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="e8b2a-110">В настоящее время командлет поддерживает обновление "автоматическое обновление" и "AutoUpdateDelayOffset" для самостоятельной среды интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="e8b2a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8b2a-111">EXAMPLES</span></span>

### <span data-ttu-id="e8b2a-112">Пример 1: обновление среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="e8b2a-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="e8b2a-113">Командлет обновляет саморазмещенную среду интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e8b2a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8b2a-114">PARAMETERS</span></span>

### <span data-ttu-id="e8b2a-115">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="e8b2a-115">-AutoUpdate</span></span>
<span data-ttu-id="e8b2a-116">Включите или отключите автоматическое обновление среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="e8b2a-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="e8b2a-118">Время в часах для автоматического обновления среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b2a-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8b2a-119">-DataFactoryName</span></span>
<span data-ttu-id="e8b2a-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-120">The data factory name.</span></span>

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

### <span data-ttu-id="e8b2a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b2a-121">-DefaultProfile</span></span>
<span data-ttu-id="e8b2a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8b2a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8b2a-123">-InputObject</span></span>
<span data-ttu-id="e8b2a-124">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="e8b2a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8b2a-125">-Name</span></span>
<span data-ttu-id="e8b2a-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="e8b2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8b2a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-128">The resource group name.</span></span>

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

### <span data-ttu-id="e8b2a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b2a-129">-ResourceId</span></span>
<span data-ttu-id="e8b2a-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e8b2a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8b2a-131">-Confirm</span></span>
<span data-ttu-id="e8b2a-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b2a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b2a-133">-WhatIf</span></span>
<span data-ttu-id="e8b2a-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b2a-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b2a-136">CommonParameters</span></span>
<span data-ttu-id="e8b2a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8b2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b2a-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8b2a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b2a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8b2a-139">INPUTS</span></span>

### <span data-ttu-id="e8b2a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e8b2a-140">System.String</span></span>

### <span data-ttu-id="e8b2a-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e8b2a-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e8b2a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b2a-142">OUTPUTS</span></span>

### <span data-ttu-id="e8b2a-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="e8b2a-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e8b2a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8b2a-144">NOTES</span></span>
<span data-ttu-id="e8b2a-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="e8b2a-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e8b2a-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8b2a-146">RELATED LINKS</span></span>

<span data-ttu-id="e8b2a-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="e8b2a-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

