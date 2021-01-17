---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 487a4592217ac725fa46ef717c6e556cc433fcb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416687"
---
# <span data-ttu-id="f5332-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5332-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f5332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5332-102">SYNOPSIS</span></span>
<span data-ttu-id="f5332-103">Обновляет время интеграции.</span><span class="sxs-lookup"><span data-stu-id="f5332-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="f5332-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5332-104">SYNTAX</span></span>

### <span data-ttu-id="f5332-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5332-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5332-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5332-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5332-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f5332-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5332-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5332-108">DESCRIPTION</span></span>
<span data-ttu-id="f5332-109">Свойства интеграции со временем запуска **update-AzDataFactoryV2IntegrationRuntime** обновляются.</span><span class="sxs-lookup"><span data-stu-id="f5332-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="f5332-110">В настоящее время для самостоятельной интеграции с этой службой можно обновить только автоматическое обновление и автоматическое обновлениеDelayOffset.</span><span class="sxs-lookup"><span data-stu-id="f5332-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="f5332-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5332-111">EXAMPLES</span></span>

### <span data-ttu-id="f5332-112">Пример 1. Обновление времени интеграции</span><span class="sxs-lookup"><span data-stu-id="f5332-112">Example 1: Updates an integration runtime</span></span>
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

<span data-ttu-id="f5332-113">Для самостоятельной интеграции с этой службой обновляется процесс самостоятельной интеграции с именем test-selfhost-ir.</span><span class="sxs-lookup"><span data-stu-id="f5332-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f5332-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5332-114">PARAMETERS</span></span>

### <span data-ttu-id="f5332-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="f5332-115">-AutoUpdate</span></span>
<span data-ttu-id="f5332-116">Включите или отключите автоматическое обновление автоматического обновления для самостоятельной интеграции.</span><span class="sxs-lookup"><span data-stu-id="f5332-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="f5332-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="f5332-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="f5332-118">Время в часах суток для автоматического обновления времени автоматического обновления интеграции.</span><span class="sxs-lookup"><span data-stu-id="f5332-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="f5332-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f5332-119">-DataFactoryName</span></span>
<span data-ttu-id="f5332-120">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="f5332-120">The data factory name.</span></span>

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

### <span data-ttu-id="f5332-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5332-121">-DefaultProfile</span></span>
<span data-ttu-id="f5332-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5332-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5332-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5332-123">-InputObject</span></span>
<span data-ttu-id="f5332-124">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="f5332-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="f5332-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f5332-125">-Name</span></span>
<span data-ttu-id="f5332-126">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="f5332-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="f5332-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5332-127">-ResourceGroupName</span></span>
<span data-ttu-id="f5332-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5332-128">The resource group name.</span></span>

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

### <span data-ttu-id="f5332-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5332-129">-ResourceId</span></span>
<span data-ttu-id="f5332-130">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="f5332-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f5332-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5332-131">-Confirm</span></span>
<span data-ttu-id="f5332-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5332-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5332-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5332-133">-WhatIf</span></span>
<span data-ttu-id="f5332-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5332-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5332-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f5332-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5332-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5332-136">CommonParameters</span></span>
<span data-ttu-id="f5332-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5332-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5332-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5332-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5332-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5332-139">INPUTS</span></span>

### <span data-ttu-id="f5332-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f5332-140">System.String</span></span>

### <span data-ttu-id="f5332-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f5332-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f5332-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5332-142">OUTPUTS</span></span>

### <span data-ttu-id="f5332-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="f5332-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="f5332-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5332-144">NOTES</span></span>
<span data-ttu-id="f5332-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="f5332-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f5332-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5332-146">RELATED LINKS</span></span>

<span data-ttu-id="f5332-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="f5332-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

