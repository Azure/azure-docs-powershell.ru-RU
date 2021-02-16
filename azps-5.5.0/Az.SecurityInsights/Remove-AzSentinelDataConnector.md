---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235772"
---
# <span data-ttu-id="ad4a2-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ad4a2-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="ad4a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4a2-103">Удаление соединитела данных.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="ad4a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad4a2-104">SYNTAX</span></span>

### <span data-ttu-id="ad4a2-105">DataConnectorId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad4a2-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad4a2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad4a2-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4a2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad4a2-107">DESCRIPTION</span></span>
<span data-ttu-id="ad4a2-108">**Cmdlet Remove-AzSentinelDataConnector** окончательно удаляет соединитель данных из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="ad4a2-109">Вы можете передать объект **DataConnector** с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="ad4a2-110">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="ad4a2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad4a2-111">EXAMPLES</span></span>

### <span data-ttu-id="ad4a2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad4a2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="ad4a2-113">Эта команда удаляет DataConnector из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="ad4a2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad4a2-114">PARAMETERS</span></span>

### <span data-ttu-id="ad4a2-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="ad4a2-115">-DataConnectorId</span></span>
<span data-ttu-id="ad4a2-116">Data Connector Id.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4a2-117">-DefaultProfile</span></span>
<span data-ttu-id="ad4a2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad4a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad4a2-119">-InputObject</span></span>
<span data-ttu-id="ad4a2-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4a2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad4a2-121">-PassThru</span></span>
<span data-ttu-id="ad4a2-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="ad4a2-122">PassThru</span></span>

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

### <span data-ttu-id="ad4a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad4a2-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4a2-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ad4a2-125">-WorkspaceName</span></span>
<span data-ttu-id="ad4a2-126">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4a2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad4a2-127">-Confirm</span></span>
<span data-ttu-id="ad4a2-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4a2-129">-WhatIf</span></span>
<span data-ttu-id="ad4a2-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad4a2-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4a2-132">CommonParameters</span></span>
<span data-ttu-id="ad4a2-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4a2-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad4a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4a2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad4a2-135">INPUTS</span></span>

### <span data-ttu-id="ad4a2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ad4a2-136">System.String</span></span>
### <span data-ttu-id="ad4a2-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ad4a2-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="ad4a2-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad4a2-138">OUTPUTS</span></span>

### <span data-ttu-id="ad4a2-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="ad4a2-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="ad4a2-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad4a2-140">NOTES</span></span>

## <span data-ttu-id="ad4a2-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad4a2-141">RELATED LINKS</span></span>
