---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236420"
---
# <span data-ttu-id="47862-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="47862-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="47862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47862-102">SYNOPSIS</span></span>
<span data-ttu-id="47862-103">Запускает набор счетчиков производительности с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="47862-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="47862-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47862-104">SYNTAX</span></span>

### <span data-ttu-id="47862-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47862-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47862-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="47862-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47862-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47862-107">DESCRIPTION</span></span>
<span data-ttu-id="47862-108">С помощью команды **Enable-AzOperationalInsightsLinuxPerformanceCollection** можно получить набор счетчиков производительности с подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="47862-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="47862-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47862-109">EXAMPLES</span></span>

## <span data-ttu-id="47862-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47862-110">PARAMETERS</span></span>

### <span data-ttu-id="47862-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47862-111">-DefaultProfile</span></span>
<span data-ttu-id="47862-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47862-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47862-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47862-113">-ResourceGroupName</span></span>
<span data-ttu-id="47862-114">Имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="47862-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47862-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="47862-115">-Workspace</span></span>
<span data-ttu-id="47862-116">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47862-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47862-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="47862-117">-WorkspaceName</span></span>
<span data-ttu-id="47862-118">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47862-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47862-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47862-119">-Confirm</span></span>
<span data-ttu-id="47862-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="47862-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47862-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47862-121">-WhatIf</span></span>
<span data-ttu-id="47862-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47862-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47862-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47862-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47862-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47862-124">CommonParameters</span></span>
<span data-ttu-id="47862-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47862-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47862-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47862-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47862-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47862-127">INPUTS</span></span>

### <span data-ttu-id="47862-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="47862-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="47862-129">System.String</span><span class="sxs-lookup"><span data-stu-id="47862-129">System.String</span></span>

## <span data-ttu-id="47862-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47862-130">OUTPUTS</span></span>

### <span data-ttu-id="47862-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="47862-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="47862-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47862-132">NOTES</span></span>
* <span data-ttu-id="47862-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="47862-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="47862-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47862-134">RELATED LINKS</span></span>

[<span data-ttu-id="47862-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="47862-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


