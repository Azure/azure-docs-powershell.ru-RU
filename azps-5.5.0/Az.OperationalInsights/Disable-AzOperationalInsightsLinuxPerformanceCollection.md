---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213324"
---
# <span data-ttu-id="06f3c-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="06f3c-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="06f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="06f3c-103">Остановка сбора счетчиков производительности с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="06f3c-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="06f3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06f3c-104">SYNTAX</span></span>

### <span data-ttu-id="06f3c-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06f3c-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06f3c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06f3c-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f3c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="06f3c-108">С помощью команды **Disable-AzOperationalInsightsLinuxPerformanceCollection** можно остановить сбор счетчиков производительности подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="06f3c-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="06f3c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06f3c-109">EXAMPLES</span></span>

## <span data-ttu-id="06f3c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06f3c-110">PARAMETERS</span></span>

### <span data-ttu-id="06f3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f3c-111">-DefaultProfile</span></span>
<span data-ttu-id="06f3c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="06f3c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06f3c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f3c-113">-ResourceGroupName</span></span>
<span data-ttu-id="06f3c-114">Имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="06f3c-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="06f3c-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="06f3c-115">-Workspace</span></span>
<span data-ttu-id="06f3c-116">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f3c-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="06f3c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06f3c-117">-WorkspaceName</span></span>
<span data-ttu-id="06f3c-118">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f3c-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="06f3c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06f3c-119">-Confirm</span></span>
<span data-ttu-id="06f3c-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f3c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f3c-121">-WhatIf</span></span>
<span data-ttu-id="06f3c-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06f3c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f3c-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="06f3c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f3c-124">CommonParameters</span></span>
<span data-ttu-id="06f3c-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06f3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f3c-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f3c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f3c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06f3c-127">INPUTS</span></span>

### <span data-ttu-id="06f3c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="06f3c-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="06f3c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="06f3c-129">System.String</span></span>

## <span data-ttu-id="06f3c-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06f3c-130">OUTPUTS</span></span>

### <span data-ttu-id="06f3c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="06f3c-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="06f3c-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06f3c-132">NOTES</span></span>
* <span data-ttu-id="06f3c-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="06f3c-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="06f3c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06f3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="06f3c-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="06f3c-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="06f3c-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="06f3c-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


