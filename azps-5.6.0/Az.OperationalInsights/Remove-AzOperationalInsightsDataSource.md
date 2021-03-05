---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 1a99f06fac37c0d96a159b0c17afc606d850ee65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989862"
---
# <span data-ttu-id="c5e23-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e23-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="c5e23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e23-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e23-103">Удаляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="c5e23-103">Deletes a data source.</span></span>

## <span data-ttu-id="c5e23-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5e23-104">SYNTAX</span></span>

### <span data-ttu-id="c5e23-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5e23-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e23-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c5e23-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e23-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e23-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e23-108">С **его учетом** удаляется источник данных.</span><span class="sxs-lookup"><span data-stu-id="c5e23-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="c5e23-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5e23-109">EXAMPLES</span></span>

## <span data-ttu-id="c5e23-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5e23-110">PARAMETERS</span></span>

### <span data-ttu-id="c5e23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e23-111">-DefaultProfile</span></span>
<span data-ttu-id="c5e23-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5e23-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5e23-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c5e23-113">-Force</span></span>
<span data-ttu-id="c5e23-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c5e23-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5e23-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c5e23-115">-Name</span></span>
<span data-ttu-id="c5e23-116">Имя источника данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c5e23-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="c5e23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e23-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5e23-118">Имя группы ресурсов, которая содержит компьютеры.</span><span class="sxs-lookup"><span data-stu-id="c5e23-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="c5e23-119">-Workspace</span><span class="sxs-lookup"><span data-stu-id="c5e23-119">-Workspace</span></span>
<span data-ttu-id="c5e23-120">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e23-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c5e23-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c5e23-121">-WorkspaceName</span></span>
<span data-ttu-id="c5e23-122">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e23-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c5e23-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5e23-123">-Confirm</span></span>
<span data-ttu-id="c5e23-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c5e23-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e23-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e23-125">-WhatIf</span></span>
<span data-ttu-id="c5e23-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e23-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e23-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c5e23-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e23-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e23-128">CommonParameters</span></span>
<span data-ttu-id="c5e23-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e23-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e23-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e23-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e23-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e23-131">INPUTS</span></span>

### <span data-ttu-id="c5e23-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c5e23-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c5e23-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c5e23-133">System.String</span></span>

## <span data-ttu-id="c5e23-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e23-134">OUTPUTS</span></span>

### <span data-ttu-id="c5e23-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="c5e23-135">System.Void</span></span>

## <span data-ttu-id="c5e23-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5e23-136">NOTES</span></span>
* <span data-ttu-id="c5e23-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="c5e23-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c5e23-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5e23-138">RELATED LINKS</span></span>

[<span data-ttu-id="c5e23-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e23-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="c5e23-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c5e23-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


