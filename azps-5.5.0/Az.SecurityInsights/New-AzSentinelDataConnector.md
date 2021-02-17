---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235801"
---
# <span data-ttu-id="b3248-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="b3248-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="b3248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3248-102">SYNOPSIS</span></span>
<span data-ttu-id="b3248-103">Создание соединитела данных.</span><span class="sxs-lookup"><span data-stu-id="b3248-103">Create a Data Connector.</span></span>

## <span data-ttu-id="b3248-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3248-104">SYNTAX</span></span>

### <span data-ttu-id="b3248-105">AzureActiveDirectory (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3248-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3248-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b3248-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3248-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="b3248-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3248-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="b3248-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3248-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="b3248-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3248-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b3248-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3248-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="b3248-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3248-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="b3248-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3248-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3248-113">DESCRIPTION</span></span>
<span data-ttu-id="b3248-114">Для создания правила оповещения **New-AzSentinelAlertRule** в указанной рабочей области создается правило аналитического оповещения.</span><span class="sxs-lookup"><span data-stu-id="b3248-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="b3248-115">Чтобы указать тип правила оповещения, необходимо указать один из параметров, например -AzureActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="b3248-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="b3248-116">У каждого типа есть разные параметры.</span><span class="sxs-lookup"><span data-stu-id="b3248-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="b3248-117">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3248-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b3248-118">Примечание. Не все соединители данных, доступные на портале, являются доступны через API.</span><span class="sxs-lookup"><span data-stu-id="b3248-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="b3248-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3248-119">EXAMPLES</span></span>

### <span data-ttu-id="b3248-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3248-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="b3248-121">В этом примере создается **dataConnector** для Центра безопасности Azure в указанной рабочей области, а затем он сохраняется в переменной $DataConnector данных.</span><span class="sxs-lookup"><span data-stu-id="b3248-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="b3248-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b3248-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="b3248-123">В этом примере создается **dataConnector** для Microsoft Cloud App Security в указанной рабочей области, а затем он сохраняется в переменной $DataConnector данных.</span><span class="sxs-lookup"><span data-stu-id="b3248-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="b3248-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3248-124">PARAMETERS</span></span>

### <span data-ttu-id="b3248-125">-Оповещения</span><span class="sxs-lookup"><span data-stu-id="b3248-125">-Alerts</span></span>
<span data-ttu-id="b3248-126">Оповещения соединитела данных</span><span class="sxs-lookup"><span data-stu-id="b3248-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="b3248-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="b3248-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="b3248-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="b3248-129">-AwsRoleArn</span></span>
<span data-ttu-id="b3248-130">Роль AWS соединитела данных AWS Arn</span><span class="sxs-lookup"><span data-stu-id="b3248-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="b3248-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="b3248-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b3248-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b3248-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="b3248-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b3248-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="b3248-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="b3248-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="b3248-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="b3248-137">-DataConnectorId</span></span>
<span data-ttu-id="b3248-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b3248-138">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3248-139">-DefaultProfile</span></span>
<span data-ttu-id="b3248-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3248-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3248-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="b3248-141">-DiscoveryLogs</span></span>
<span data-ttu-id="b3248-142">Журналы обнаружения соединители данных</span><span class="sxs-lookup"><span data-stu-id="b3248-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="b3248-143">-Exchange</span></span>
<span data-ttu-id="b3248-144">Data Connector Exchange</span><span class="sxs-lookup"><span data-stu-id="b3248-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-145">-Индикаторы</span><span class="sxs-lookup"><span data-stu-id="b3248-145">-Indicators</span></span>
<span data-ttu-id="b3248-146">Индикаторы соединители данных</span><span class="sxs-lookup"><span data-stu-id="b3248-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="b3248-147">-Logs</span></span>
<span data-ttu-id="b3248-148">Журналы соединители данных</span><span class="sxs-lookup"><span data-stu-id="b3248-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="b3248-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="b3248-150">Data Connector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b3248-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="b3248-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="b3248-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b3248-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="b3248-153">-Office365</span></span>
<span data-ttu-id="b3248-154">Data Connector Office 365</span><span class="sxs-lookup"><span data-stu-id="b3248-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3248-155">-ResourceGroupName</span></span>
<span data-ttu-id="b3248-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b3248-156">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="b3248-157">-SharePoint</span></span>
<span data-ttu-id="b3248-158">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="b3248-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3248-159">-SubscriptionId</span></span>
<span data-ttu-id="b3248-160">Data connector Subscription Id</span><span class="sxs-lookup"><span data-stu-id="b3248-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="b3248-161">-ThreatIntelligence</span></span>
<span data-ttu-id="b3248-162">Data Connector Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="b3248-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b3248-163">-WorkspaceName</span></span>
<span data-ttu-id="b3248-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="b3248-164">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3248-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3248-165">-Confirm</span></span>
<span data-ttu-id="b3248-166">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3248-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3248-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3248-167">-WhatIf</span></span>
<span data-ttu-id="b3248-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3248-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3248-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b3248-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3248-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3248-170">CommonParameters</span></span>
<span data-ttu-id="b3248-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3248-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3248-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3248-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3248-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3248-173">INPUTS</span></span>

### <span data-ttu-id="b3248-174">Нет</span><span class="sxs-lookup"><span data-stu-id="b3248-174">None</span></span>
## <span data-ttu-id="b3248-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3248-175">OUTPUTS</span></span>

### <span data-ttu-id="b3248-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="b3248-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="b3248-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3248-177">NOTES</span></span>

## <span data-ttu-id="b3248-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3248-178">RELATED LINKS</span></span>
