---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505949"
---
# <span data-ttu-id="3d00a-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d00a-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="3d00a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d00a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d00a-103">Создание и обновление группы безопасности устройств</span><span class="sxs-lookup"><span data-stu-id="3d00a-103">Create or update device security group</span></span>

## <span data-ttu-id="3d00a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d00a-104">SYNTAX</span></span>

### <span data-ttu-id="3d00a-105">ResourceIdLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d00a-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d00a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3d00a-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d00a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d00a-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d00a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d00a-108">DESCRIPTION</span></span>
<span data-ttu-id="3d00a-109">С Set-AzDeviceSecurityGroup создает или обновляет группу безопасности устройств, определенное в решении для защиты iot.</span><span class="sxs-lookup"><span data-stu-id="3d00a-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="3d00a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d00a-110">EXAMPLES</span></span>

### <span data-ttu-id="3d00a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d00a-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="3d00a-112">Обновление существующей группы безопасности устройств из концентратора IoT "/subscriptions/XXXXXXXX-XXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" с типом правил "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="3d00a-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="3d00a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d00a-113">PARAMETERS</span></span>

### <span data-ttu-id="3d00a-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="3d00a-114">-AllowlistRule</span></span>
<span data-ttu-id="3d00a-115">Разрешить правила списка.</span><span class="sxs-lookup"><span data-stu-id="3d00a-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d00a-116">-DefaultProfile</span></span>
<span data-ttu-id="3d00a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d00a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d00a-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="3d00a-118">-DenylistRule</span></span>
<span data-ttu-id="3d00a-119">Запретить правила списка.</span><span class="sxs-lookup"><span data-stu-id="3d00a-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="3d00a-120">-HubResourceId</span></span>
<span data-ttu-id="3d00a-121">IoT Hub resource Id.</span><span class="sxs-lookup"><span data-stu-id="3d00a-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d00a-122">-InputObject</span></span>
<span data-ttu-id="3d00a-123">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="3d00a-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3d00a-124">-Name</span></span>
<span data-ttu-id="3d00a-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d00a-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d00a-126">-ResourceId</span></span>
<span data-ttu-id="3d00a-127">ИД ресурса безопасности, для который требуется вызвать команду.</span><span class="sxs-lookup"><span data-stu-id="3d00a-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="3d00a-128">-ThresholdRule</span></span>
<span data-ttu-id="3d00a-129">Пороговые значения правил.</span><span class="sxs-lookup"><span data-stu-id="3d00a-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="3d00a-130">-TimeWindowRule</span></span>
<span data-ttu-id="3d00a-131">Правила окне времени.</span><span class="sxs-lookup"><span data-stu-id="3d00a-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d00a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d00a-132">-Confirm</span></span>
<span data-ttu-id="3d00a-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d00a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d00a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d00a-134">-WhatIf</span></span>
<span data-ttu-id="3d00a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d00a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d00a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3d00a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d00a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d00a-137">CommonParameters</span></span>
<span data-ttu-id="3d00a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d00a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d00a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d00a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d00a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d00a-140">INPUTS</span></span>

### <span data-ttu-id="3d00a-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="3d00a-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="3d00a-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="3d00a-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="3d00a-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="3d00a-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="3d00a-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="3d00a-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="3d00a-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d00a-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="3d00a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3d00a-146">System.String</span></span>

## <span data-ttu-id="3d00a-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d00a-147">OUTPUTS</span></span>

### <span data-ttu-id="3d00a-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d00a-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="3d00a-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d00a-149">NOTES</span></span>

## <span data-ttu-id="3d00a-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d00a-150">RELATED LINKS</span></span>
