---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e923d413b889583578efb0ac81f9eb6aeadf72fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977811"
---
# <span data-ttu-id="d4b6b-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="d4b6b-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="d4b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b6b-103">Определяет настраиваемую политику сбора журналов.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="d4b6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4b6b-104">SYNTAX</span></span>

### <span data-ttu-id="d4b6b-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4b6b-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b6b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d4b6b-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4b6b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4b6b-107">DESCRIPTION</span></span>
<span data-ttu-id="d4b6b-108">**Новый-AzOperationalInsightsCustomLogDataSource** определяет настраиваемую политику сбора журналов.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="d4b6b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4b6b-109">EXAMPLES</span></span>

## <span data-ttu-id="d4b6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4b6b-110">PARAMETERS</span></span>

### <span data-ttu-id="d4b6b-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="d4b6b-111">-CustomLogRawJson</span></span>
<span data-ttu-id="d4b6b-112">Настраиваемая политика сбора определяется как необработанные строки нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="d4b6b-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b6b-113">-DefaultProfile</span></span>
<span data-ttu-id="d4b6b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d4b6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4b6b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d4b6b-115">-Force</span></span>
<span data-ttu-id="d4b6b-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4b6b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d4b6b-117">-Name</span></span>
<span data-ttu-id="d4b6b-118">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4b6b-120">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d4b6b-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d4b6b-121">-Workspace</span></span>
<span data-ttu-id="d4b6b-122">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d4b6b-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4b6b-123">-WorkspaceName</span></span>
<span data-ttu-id="d4b6b-124">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d4b6b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4b6b-125">-Confirm</span></span>
<span data-ttu-id="d4b6b-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b6b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b6b-127">-WhatIf</span></span>
<span data-ttu-id="d4b6b-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b6b-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b6b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b6b-130">CommonParameters</span></span>
<span data-ttu-id="d4b6b-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4b6b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b6b-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b6b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b6b-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4b6b-133">INPUTS</span></span>

### <span data-ttu-id="d4b6b-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d4b6b-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d4b6b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d4b6b-135">System.String</span></span>

## <span data-ttu-id="d4b6b-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4b6b-136">OUTPUTS</span></span>

### <span data-ttu-id="d4b6b-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d4b6b-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d4b6b-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4b6b-138">NOTES</span></span>

## <span data-ttu-id="d4b6b-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4b6b-139">RELATED LINKS</span></span>

[<span data-ttu-id="d4b6b-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d4b6b-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="d4b6b-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d4b6b-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


