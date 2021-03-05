---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978131"
---
# <span data-ttu-id="50f4f-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="50f4f-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="50f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="50f4f-103">Удаление соединитела данных.</span><span class="sxs-lookup"><span data-stu-id="50f4f-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="50f4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50f4f-104">SYNTAX</span></span>

### <span data-ttu-id="50f4f-105">DataConnectorId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50f4f-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f4f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="50f4f-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50f4f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50f4f-107">DESCRIPTION</span></span>
<span data-ttu-id="50f4f-108">**Cmdlet Remove-AzSentinelDataConnector** окончательно удаляет соединитель данных из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="50f4f-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="50f4f-109">Вы можете передать объект **DataConnector** с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="50f4f-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="50f4f-110">С помощью переменных Confirm и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50f4f-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="50f4f-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50f4f-111">EXAMPLES</span></span>

### <span data-ttu-id="50f4f-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50f4f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="50f4f-113">Эта команда удаляет DataConnector из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="50f4f-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="50f4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50f4f-114">PARAMETERS</span></span>

### <span data-ttu-id="50f4f-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="50f4f-115">-DataConnectorId</span></span>
<span data-ttu-id="50f4f-116">Data Connector Id.</span><span class="sxs-lookup"><span data-stu-id="50f4f-116">Data Connector Id.</span></span>

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

### <span data-ttu-id="50f4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f4f-117">-DefaultProfile</span></span>
<span data-ttu-id="50f4f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50f4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50f4f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50f4f-119">-InputObject</span></span>
<span data-ttu-id="50f4f-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="50f4f-120">InputObject.</span></span>

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

### <span data-ttu-id="50f4f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50f4f-121">-PassThru</span></span>
<span data-ttu-id="50f4f-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="50f4f-122">PassThru</span></span>

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

### <span data-ttu-id="50f4f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f4f-123">-ResourceGroupName</span></span>
<span data-ttu-id="50f4f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50f4f-124">Resource group name.</span></span>

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

### <span data-ttu-id="50f4f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50f4f-125">-WorkspaceName</span></span>
<span data-ttu-id="50f4f-126">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="50f4f-126">Workspace Name.</span></span>

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

### <span data-ttu-id="50f4f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50f4f-127">-Confirm</span></span>
<span data-ttu-id="50f4f-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50f4f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50f4f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f4f-129">-WhatIf</span></span>
<span data-ttu-id="50f4f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50f4f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50f4f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50f4f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50f4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f4f-132">CommonParameters</span></span>
<span data-ttu-id="50f4f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f4f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50f4f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f4f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50f4f-135">INPUTS</span></span>

### <span data-ttu-id="50f4f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="50f4f-136">System.String</span></span>
### <span data-ttu-id="50f4f-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="50f4f-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="50f4f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50f4f-138">OUTPUTS</span></span>

### <span data-ttu-id="50f4f-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="50f4f-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="50f4f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50f4f-140">NOTES</span></span>

## <span data-ttu-id="50f4f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50f4f-141">RELATED LINKS</span></span>
