---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0cd64af058ecf9bbc1f42178d263fcf20cabc75f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401676"
---
# <span data-ttu-id="2d6f9-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2d6f9-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="2d6f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6f9-103">Запускает коллекцию настраиваемого журнала на компьютерах Linux.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="2d6f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d6f9-104">SYNTAX</span></span>

### <span data-ttu-id="2d6f9-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d6f9-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d6f9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d6f9-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d6f9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d6f9-107">DESCRIPTION</span></span>
<span data-ttu-id="2d6f9-108">С помощью cmdlet **Enable-AzOperationalInsightsLinuxCustomLogCollection** можно получить набор настраиваемого журнала с подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="2d6f9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d6f9-109">EXAMPLES</span></span>

## <span data-ttu-id="2d6f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d6f9-110">PARAMETERS</span></span>

### <span data-ttu-id="2d6f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6f9-111">-DefaultProfile</span></span>
<span data-ttu-id="2d6f9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d6f9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d6f9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d6f9-113">-ResourceGroupName</span></span>
<span data-ttu-id="2d6f9-114">Имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="2d6f9-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="2d6f9-115">-Workspace</span></span>
<span data-ttu-id="2d6f9-116">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d6f9-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d6f9-117">-WorkspaceName</span></span>
<span data-ttu-id="2d6f9-118">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d6f9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d6f9-119">-Confirm</span></span>
<span data-ttu-id="2d6f9-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d6f9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d6f9-121">-WhatIf</span></span>
<span data-ttu-id="2d6f9-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d6f9-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d6f9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6f9-124">CommonParameters</span></span>
<span data-ttu-id="2d6f9-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d6f9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6f9-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d6f9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6f9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d6f9-127">INPUTS</span></span>

### <span data-ttu-id="2d6f9-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d6f9-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2d6f9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2d6f9-129">System.String</span></span>

## <span data-ttu-id="2d6f9-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d6f9-130">OUTPUTS</span></span>

### <span data-ttu-id="2d6f9-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2d6f9-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2d6f9-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d6f9-132">NOTES</span></span>
* <span data-ttu-id="2d6f9-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="2d6f9-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2d6f9-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d6f9-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d6f9-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2d6f9-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


