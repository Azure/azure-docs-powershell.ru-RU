---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425020"
---
# <span data-ttu-id="87009-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="87009-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="87009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87009-102">SYNOPSIS</span></span>
<span data-ttu-id="87009-103">Запускает коллекцию журналов IIS с компьютеров в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="87009-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="87009-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87009-104">SYNTAX</span></span>

### <span data-ttu-id="87009-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87009-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87009-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="87009-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87009-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87009-107">DESCRIPTION</span></span>
<span data-ttu-id="87009-108">С помощью cmdlet **Enable-AzOperationalInsightsIISLogCollection** запускается коллекция журналов IIS с подключенных компьютеров в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="87009-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="87009-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87009-109">EXAMPLES</span></span>

## <span data-ttu-id="87009-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87009-110">PARAMETERS</span></span>

### <span data-ttu-id="87009-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87009-111">-DefaultProfile</span></span>
<span data-ttu-id="87009-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="87009-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87009-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87009-113">-ResourceGroupName</span></span>
<span data-ttu-id="87009-114">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="87009-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="87009-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="87009-115">-Workspace</span></span>
<span data-ttu-id="87009-116">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87009-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="87009-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="87009-117">-WorkspaceName</span></span>
<span data-ttu-id="87009-118">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87009-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="87009-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87009-119">-Confirm</span></span>
<span data-ttu-id="87009-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87009-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87009-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87009-121">-WhatIf</span></span>
<span data-ttu-id="87009-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87009-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87009-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="87009-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87009-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87009-124">CommonParameters</span></span>
<span data-ttu-id="87009-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87009-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87009-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87009-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87009-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87009-127">INPUTS</span></span>

### <span data-ttu-id="87009-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="87009-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="87009-129">System.String</span><span class="sxs-lookup"><span data-stu-id="87009-129">System.String</span></span>

## <span data-ttu-id="87009-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87009-130">OUTPUTS</span></span>

### <span data-ttu-id="87009-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="87009-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="87009-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87009-132">NOTES</span></span>

## <span data-ttu-id="87009-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87009-133">RELATED LINKS</span></span>

[<span data-ttu-id="87009-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="87009-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


