---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729839"
---
# <span data-ttu-id="72e04-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="72e04-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="72e04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72e04-102">SYNOPSIS</span></span>
<span data-ttu-id="72e04-103">Удаляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="72e04-103">Deletes a data source.</span></span>

## <span data-ttu-id="72e04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72e04-104">SYNTAX</span></span>

### <span data-ttu-id="72e04-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72e04-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72e04-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="72e04-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72e04-107">DESCRIPTION</span></span>
<span data-ttu-id="72e04-108">Командлет **Remove-AzOperationalInsightsDataSource** удаляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="72e04-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="72e04-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72e04-109">EXAMPLES</span></span>

## <span data-ttu-id="72e04-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72e04-110">PARAMETERS</span></span>

### <span data-ttu-id="72e04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e04-111">-DefaultProfile</span></span>
<span data-ttu-id="72e04-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="72e04-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72e04-113">-Force</span><span class="sxs-lookup"><span data-stu-id="72e04-113">-Force</span></span>
<span data-ttu-id="72e04-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="72e04-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72e04-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72e04-115">-Name</span></span>
<span data-ttu-id="72e04-116">Указывает имя источника данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="72e04-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="72e04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e04-117">-ResourceGroupName</span></span>
<span data-ttu-id="72e04-118">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="72e04-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="72e04-119">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="72e04-119">-Workspace</span></span>
<span data-ttu-id="72e04-120">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="72e04-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="72e04-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72e04-121">-WorkspaceName</span></span>
<span data-ttu-id="72e04-122">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="72e04-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="72e04-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72e04-123">-Confirm</span></span>
<span data-ttu-id="72e04-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72e04-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e04-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e04-125">-WhatIf</span></span>
<span data-ttu-id="72e04-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72e04-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72e04-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72e04-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e04-128">CommonParameters</span></span>
<span data-ttu-id="72e04-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72e04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e04-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e04-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e04-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72e04-131">INPUTS</span></span>

### <span data-ttu-id="72e04-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="72e04-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="72e04-133">System. String</span><span class="sxs-lookup"><span data-stu-id="72e04-133">System.String</span></span>

## <span data-ttu-id="72e04-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72e04-134">OUTPUTS</span></span>

### <span data-ttu-id="72e04-135">System. void</span><span class="sxs-lookup"><span data-stu-id="72e04-135">System.Void</span></span>

## <span data-ttu-id="72e04-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="72e04-136">NOTES</span></span>
* <span data-ttu-id="72e04-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="72e04-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="72e04-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72e04-138">RELATED LINKS</span></span>

[<span data-ttu-id="72e04-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="72e04-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="72e04-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="72e04-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


