---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 7eb4675e44a252feec913b531a30f9062f6b791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976344"
---
# <span data-ttu-id="ea03d-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ea03d-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="ea03d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea03d-102">SYNOPSIS</span></span>
<span data-ttu-id="ea03d-103">Создание соединитела данных.</span><span class="sxs-lookup"><span data-stu-id="ea03d-103">Create a Data Connector.</span></span>

## <span data-ttu-id="ea03d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea03d-104">SYNTAX</span></span>

### <span data-ttu-id="ea03d-105">AzureActiveDirectory (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea03d-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea03d-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ea03d-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea03d-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="ea03d-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea03d-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="ea03d-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea03d-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="ea03d-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea03d-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ea03d-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea03d-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="ea03d-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea03d-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="ea03d-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea03d-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea03d-113">DESCRIPTION</span></span>
<span data-ttu-id="ea03d-114">Для создания правила оповещения **New-AzSentinelAlertRule** в указанной рабочей области создается правило аналитики.</span><span class="sxs-lookup"><span data-stu-id="ea03d-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="ea03d-115">Чтобы создать правило оповещения, необходимо указать один из параметров, например -AzureActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="ea03d-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="ea03d-116">У каждого типа есть разные параметры.</span><span class="sxs-lookup"><span data-stu-id="ea03d-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="ea03d-117">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea03d-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ea03d-118">Примечание. Не все соединители данных, доступные на портале, являются доступны через API.</span><span class="sxs-lookup"><span data-stu-id="ea03d-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="ea03d-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea03d-119">EXAMPLES</span></span>

### <span data-ttu-id="ea03d-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea03d-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="ea03d-121">В этом примере создается **dataConnector** для Центра безопасности Azure в указанной рабочей области, а затем $DataConnector переменной.</span><span class="sxs-lookup"><span data-stu-id="ea03d-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="ea03d-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea03d-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="ea03d-123">В этом примере создается **dataConnector** для Microsoft Cloud App Security в указанной рабочей области, а затем он сохраняется в переменной $DataConnector данных.</span><span class="sxs-lookup"><span data-stu-id="ea03d-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="ea03d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea03d-124">PARAMETERS</span></span>

### <span data-ttu-id="ea03d-125">-Оповещения</span><span class="sxs-lookup"><span data-stu-id="ea03d-125">-Alerts</span></span>
<span data-ttu-id="ea03d-126">Оповещения соединитела данных</span><span class="sxs-lookup"><span data-stu-id="ea03d-126">Data Connector Alerts</span></span>

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

### <span data-ttu-id="ea03d-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="ea03d-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="ea03d-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="ea03d-128">Data Connector Amazon Web Services Cloud Trail</span></span>

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

### <span data-ttu-id="ea03d-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="ea03d-129">-AwsRoleArn</span></span>
<span data-ttu-id="ea03d-130">Роль AWS соединитела данных AWS Arn</span><span class="sxs-lookup"><span data-stu-id="ea03d-130">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="ea03d-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ea03d-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="ea03d-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ea03d-132">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="ea03d-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ea03d-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="ea03d-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ea03d-134">Data Connector Azure Advanced Threat Protection</span></span>

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

### <span data-ttu-id="ea03d-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="ea03d-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="ea03d-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="ea03d-136">Data Connector Azure Security Center</span></span>

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

### <span data-ttu-id="ea03d-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="ea03d-137">-DataConnectorId</span></span>
<span data-ttu-id="ea03d-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ea03d-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="ea03d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea03d-139">-DefaultProfile</span></span>
<span data-ttu-id="ea03d-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea03d-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea03d-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="ea03d-141">-DiscoveryLogs</span></span>
<span data-ttu-id="ea03d-142">Журналы обнаружения соединители данных</span><span class="sxs-lookup"><span data-stu-id="ea03d-142">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="ea03d-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="ea03d-143">-Exchange</span></span>
<span data-ttu-id="ea03d-144">Data Connector Exchange</span><span class="sxs-lookup"><span data-stu-id="ea03d-144">Data Connector Exchange</span></span>

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

### <span data-ttu-id="ea03d-145">-Индикаторы</span><span class="sxs-lookup"><span data-stu-id="ea03d-145">-Indicators</span></span>
<span data-ttu-id="ea03d-146">Индикаторы соединители данных</span><span class="sxs-lookup"><span data-stu-id="ea03d-146">Data Connector Indicators</span></span>

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

### <span data-ttu-id="ea03d-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="ea03d-147">-Logs</span></span>
<span data-ttu-id="ea03d-148">Журналы соединители данных</span><span class="sxs-lookup"><span data-stu-id="ea03d-148">Data Connector Logs</span></span>

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

### <span data-ttu-id="ea03d-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="ea03d-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="ea03d-150">Data Connector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="ea03d-150">Data Connector Microsoft Cloud App Security</span></span>

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

### <span data-ttu-id="ea03d-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ea03d-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="ea03d-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ea03d-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

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

### <span data-ttu-id="ea03d-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="ea03d-153">-Office365</span></span>
<span data-ttu-id="ea03d-154">Data Connector Office 365</span><span class="sxs-lookup"><span data-stu-id="ea03d-154">Data Connector Office 365</span></span>

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

### <span data-ttu-id="ea03d-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea03d-155">-ResourceGroupName</span></span>
<span data-ttu-id="ea03d-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ea03d-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="ea03d-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea03d-157">-SharePoint</span></span>
<span data-ttu-id="ea03d-158">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea03d-158">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="ea03d-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea03d-159">-SubscriptionId</span></span>
<span data-ttu-id="ea03d-160">Data connector Subscription Id</span><span class="sxs-lookup"><span data-stu-id="ea03d-160">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="ea03d-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="ea03d-161">-ThreatIntelligence</span></span>
<span data-ttu-id="ea03d-162">Data Connector Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="ea03d-162">Data Connector Threat Intelligence</span></span>

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

### <span data-ttu-id="ea03d-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ea03d-163">-WorkspaceName</span></span>
<span data-ttu-id="ea03d-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ea03d-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="ea03d-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea03d-165">-Confirm</span></span>
<span data-ttu-id="ea03d-166">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ea03d-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea03d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea03d-167">-WhatIf</span></span>
<span data-ttu-id="ea03d-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea03d-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea03d-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea03d-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea03d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea03d-170">CommonParameters</span></span>
<span data-ttu-id="ea03d-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea03d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea03d-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea03d-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea03d-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea03d-173">INPUTS</span></span>

### <span data-ttu-id="ea03d-174">Нет</span><span class="sxs-lookup"><span data-stu-id="ea03d-174">None</span></span>
## <span data-ttu-id="ea03d-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea03d-175">OUTPUTS</span></span>

### <span data-ttu-id="ea03d-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ea03d-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="ea03d-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea03d-177">NOTES</span></span>

## <span data-ttu-id="ea03d-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea03d-178">RELATED LINKS</span></span>
