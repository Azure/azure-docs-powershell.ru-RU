---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225257"
---
# <span data-ttu-id="73304-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="73304-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="73304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73304-102">SYNOPSIS</span></span>
<span data-ttu-id="73304-103">Обновление соединитела данных.</span><span class="sxs-lookup"><span data-stu-id="73304-103">Update a Data Connector.</span></span>

## <span data-ttu-id="73304-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73304-104">SYNTAX</span></span>

### <span data-ttu-id="73304-105">DataConnectorId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73304-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73304-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="73304-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73304-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="73304-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73304-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73304-108">DESCRIPTION</span></span>
<span data-ttu-id="73304-109">В этом рабочей области соединитель **Update-AzSentinelDataConnector** обновляет соединитель данных.</span><span class="sxs-lookup"><span data-stu-id="73304-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="73304-110">Объект **DataConnector** можно передать в качестве параметра или с помощью оператора конвейера. Кроме того, можно указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="73304-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="73304-111">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73304-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="73304-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73304-112">EXAMPLES</span></span>

### <span data-ttu-id="73304-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73304-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="73304-114">Команда получает соединители данных по *DataConnectorId* и задает состояние *"Отключение* оповещений". </span><span class="sxs-lookup"><span data-stu-id="73304-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="73304-115">Все остальные свойства остаются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="73304-115">All other properties remain the same.</span></span>

## <span data-ttu-id="73304-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73304-116">PARAMETERS</span></span>

### <span data-ttu-id="73304-117">-Оповещения</span><span class="sxs-lookup"><span data-stu-id="73304-117">-Alerts</span></span>
<span data-ttu-id="73304-118">Оповещения соединитела данных</span><span class="sxs-lookup"><span data-stu-id="73304-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="73304-119">-AwsRoleArn</span></span>
<span data-ttu-id="73304-120">Роль AWS соединитела данных AWS Arn</span><span class="sxs-lookup"><span data-stu-id="73304-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="73304-121">-DataConnectorId</span></span>
<span data-ttu-id="73304-122">Data Connector Id.</span><span class="sxs-lookup"><span data-stu-id="73304-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73304-123">-DefaultProfile</span></span>
<span data-ttu-id="73304-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73304-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="73304-125">-DiscoveryLogs</span></span>
<span data-ttu-id="73304-126">Журналы обнаружения соединители данных</span><span class="sxs-lookup"><span data-stu-id="73304-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="73304-127">-Exchange</span></span>
<span data-ttu-id="73304-128">Data Connector Exchange</span><span class="sxs-lookup"><span data-stu-id="73304-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-129">-Индикаторы</span><span class="sxs-lookup"><span data-stu-id="73304-129">-Indicators</span></span>
<span data-ttu-id="73304-130">Индикаторы соединители данных</span><span class="sxs-lookup"><span data-stu-id="73304-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73304-131">-InputObject</span></span>
<span data-ttu-id="73304-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="73304-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73304-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="73304-133">-Logs</span></span>
<span data-ttu-id="73304-134">Журналы соединители данных</span><span class="sxs-lookup"><span data-stu-id="73304-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73304-135">-ResourceGroupName</span></span>
<span data-ttu-id="73304-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73304-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73304-137">-ResourceId</span></span>
<span data-ttu-id="73304-138">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="73304-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73304-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="73304-139">-SharePoint</span></span>
<span data-ttu-id="73304-140">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="73304-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73304-141">-SubscriptionId</span></span>
<span data-ttu-id="73304-142">Data connector Subscription Id</span><span class="sxs-lookup"><span data-stu-id="73304-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73304-143">-WorkspaceName</span></span>
<span data-ttu-id="73304-144">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="73304-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73304-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73304-145">-Confirm</span></span>
<span data-ttu-id="73304-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73304-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73304-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73304-147">-WhatIf</span></span>
<span data-ttu-id="73304-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73304-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73304-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73304-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73304-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73304-150">CommonParameters</span></span>
<span data-ttu-id="73304-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73304-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73304-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73304-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73304-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73304-153">INPUTS</span></span>

### <span data-ttu-id="73304-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="73304-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="73304-155">System.String</span><span class="sxs-lookup"><span data-stu-id="73304-155">System.String</span></span>

## <span data-ttu-id="73304-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73304-156">OUTPUTS</span></span>

### <span data-ttu-id="73304-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="73304-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="73304-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73304-158">NOTES</span></span>

## <span data-ttu-id="73304-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73304-159">RELATED LINKS</span></span>
