---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401700"
---
# <span data-ttu-id="9f68b-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9f68b-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="9f68b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f68b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f68b-103">Запускает коллекцию данных для системного анализа с компьютеров Linux.</span><span class="sxs-lookup"><span data-stu-id="9f68b-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="9f68b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f68b-104">SYNTAX</span></span>

### <span data-ttu-id="9f68b-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f68b-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f68b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9f68b-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f68b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f68b-107">DESCRIPTION</span></span>
<span data-ttu-id="9f68b-108">С помощью cmdlet **Enable-AzOperationalInsightsLinuxSyslogCollection** можно получить набор данных для системного анализа с подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9f68b-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="9f68b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f68b-109">EXAMPLES</span></span>

## <span data-ttu-id="9f68b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f68b-110">PARAMETERS</span></span>

### <span data-ttu-id="9f68b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f68b-111">-DefaultProfile</span></span>
<span data-ttu-id="9f68b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9f68b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f68b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f68b-113">-ResourceGroupName</span></span>
<span data-ttu-id="9f68b-114">Имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="9f68b-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9f68b-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="9f68b-115">-Workspace</span></span>
<span data-ttu-id="9f68b-116">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f68b-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9f68b-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f68b-117">-WorkspaceName</span></span>
<span data-ttu-id="9f68b-118">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f68b-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9f68b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f68b-119">-Confirm</span></span>
<span data-ttu-id="9f68b-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f68b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f68b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f68b-121">-WhatIf</span></span>
<span data-ttu-id="9f68b-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f68b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f68b-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f68b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f68b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f68b-124">CommonParameters</span></span>
<span data-ttu-id="9f68b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f68b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f68b-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f68b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f68b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f68b-127">INPUTS</span></span>

### <span data-ttu-id="9f68b-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9f68b-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9f68b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9f68b-129">System.String</span></span>

## <span data-ttu-id="9f68b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f68b-130">OUTPUTS</span></span>

### <span data-ttu-id="9f68b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9f68b-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9f68b-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f68b-132">NOTES</span></span>
* <span data-ttu-id="9f68b-133">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="9f68b-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9f68b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f68b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f68b-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9f68b-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="9f68b-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="9f68b-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


