---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 8ec48fe995d6f6be817d418714262706436ebf3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997646"
---
# <span data-ttu-id="37774-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="37774-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="37774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37774-102">SYNOPSIS</span></span>
<span data-ttu-id="37774-103">Остановка сбора журналов IIS с компьютеров.</span><span class="sxs-lookup"><span data-stu-id="37774-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="37774-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37774-104">SYNTAX</span></span>

### <span data-ttu-id="37774-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="37774-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37774-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="37774-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37774-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37774-107">DESCRIPTION</span></span>
<span data-ttu-id="37774-108">С помощью cmdlet **Disable-AzOperationalInsightsIISLogCollection** можно остановить сбор журналов IIS с подключенных компьютеров в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="37774-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="37774-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37774-109">EXAMPLES</span></span>

## <span data-ttu-id="37774-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37774-110">PARAMETERS</span></span>

### <span data-ttu-id="37774-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37774-111">-DefaultProfile</span></span>
<span data-ttu-id="37774-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37774-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37774-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37774-113">-ResourceGroupName</span></span>
<span data-ttu-id="37774-114">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="37774-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="37774-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="37774-115">-Workspace</span></span>
<span data-ttu-id="37774-116">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37774-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="37774-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37774-117">-WorkspaceName</span></span>
<span data-ttu-id="37774-118">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37774-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="37774-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37774-119">-Confirm</span></span>
<span data-ttu-id="37774-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="37774-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37774-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37774-121">-WhatIf</span></span>
<span data-ttu-id="37774-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37774-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37774-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="37774-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37774-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37774-124">CommonParameters</span></span>
<span data-ttu-id="37774-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37774-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37774-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37774-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37774-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37774-127">INPUTS</span></span>

### <span data-ttu-id="37774-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="37774-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="37774-129">System.String</span><span class="sxs-lookup"><span data-stu-id="37774-129">System.String</span></span>

## <span data-ttu-id="37774-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37774-130">OUTPUTS</span></span>

### <span data-ttu-id="37774-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="37774-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="37774-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37774-132">NOTES</span></span>
* <span data-ttu-id="37774-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="37774-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="37774-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37774-134">RELATED LINKS</span></span>

[<span data-ttu-id="37774-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="37774-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


