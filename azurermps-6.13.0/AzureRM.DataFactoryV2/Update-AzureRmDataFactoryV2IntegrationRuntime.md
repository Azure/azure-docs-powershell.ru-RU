---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 2c20752dd1e29962f128f687344b3b165f0a09ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564580"
---
# <span data-ttu-id="2c4a5-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c4a5-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2c4a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4a5-103">Обновляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c4a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c4a5-104">SYNTAX</span></span>

### <span data-ttu-id="2c4a5-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c4a5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4a5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4a5-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c4a5-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2c4a5-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c4a5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c4a5-108">DESCRIPTION</span></span>
<span data-ttu-id="2c4a5-109">Командлет **Update-AzureRmDataFactoryV2IntegrationRuntime** обновляет свойства среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="2c4a5-110">В настоящее время командлет поддерживает обновление "автоматическое обновление" и "AutoUpdateDelayOffset" для самостоятельной среды интеграции.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="2c4a5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c4a5-111">EXAMPLES</span></span>

### <span data-ttu-id="2c4a5-112">Пример 1: обновление среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="2c4a5-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="2c4a5-113">Командлет обновляет саморазмещенную среду интеграции с именем Test-SelfHost-IR.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="2c4a5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c4a5-114">PARAMETERS</span></span>

### <span data-ttu-id="2c4a5-115">-Автоматическое обновление</span><span class="sxs-lookup"><span data-stu-id="2c4a5-115">-AutoUpdate</span></span>
<span data-ttu-id="2c4a5-116">Включите или отключите автоматическое обновление среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="2c4a5-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="2c4a5-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="2c4a5-118">Время в часах для автоматического обновления среды выполнения интеграции с самостоятельным размещением.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="2c4a5-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c4a5-119">-DataFactoryName</span></span>
<span data-ttu-id="2c4a5-120">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-120">The data factory name.</span></span>

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

### <span data-ttu-id="2c4a5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4a5-121">-DefaultProfile</span></span>
<span data-ttu-id="2c4a5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c4a5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c4a5-123">-InputObject</span></span>
<span data-ttu-id="2c4a5-124">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="2c4a5-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c4a5-125">-Name</span></span>
<span data-ttu-id="2c4a5-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="2c4a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="2c4a5-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-128">The resource group name.</span></span>

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

### <span data-ttu-id="2c4a5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c4a5-129">-ResourceId</span></span>
<span data-ttu-id="2c4a5-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2c4a5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c4a5-131">-Confirm</span></span>
<span data-ttu-id="2c4a5-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4a5-133">-WhatIf</span></span>
<span data-ttu-id="2c4a5-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c4a5-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4a5-136">CommonParameters</span></span>
<span data-ttu-id="2c4a5-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c4a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4a5-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4a5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4a5-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c4a5-139">INPUTS</span></span>

### <span data-ttu-id="2c4a5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2c4a5-140">System.String</span></span>

### <span data-ttu-id="2c4a5-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c4a5-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="2c4a5-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c4a5-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2c4a5-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c4a5-143">OUTPUTS</span></span>

### <span data-ttu-id="2c4a5-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="2c4a5-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="2c4a5-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c4a5-145">NOTES</span></span>
<span data-ttu-id="2c4a5-146">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="2c4a5-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="2c4a5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c4a5-147">RELATED LINKS</span></span>

<span data-ttu-id="2c4a5-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="2c4a5-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

