---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422604"
---
# <span data-ttu-id="a5d44-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="a5d44-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="a5d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d44-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d44-103">Регистрирует средство в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="a5d44-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="a5d44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5d44-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5d44-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5d44-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d44-106">Регистрирует средство в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="a5d44-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="a5d44-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5d44-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d44-108">Пример 1. Инструмент REgister.</span><span class="sxs-lookup"><span data-stu-id="a5d44-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="a5d44-109">Регистрирует средство в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="a5d44-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="a5d44-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5d44-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d44-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a5d44-111">-AcceptLanguage</span></span>
<span data-ttu-id="a5d44-112">Стандартный заметив запроса.</span><span class="sxs-lookup"><span data-stu-id="a5d44-112">Standard request header.</span></span>
<span data-ttu-id="a5d44-113">Используется службой для ответа на клиент на соответствующем языке.</span><span class="sxs-lookup"><span data-stu-id="a5d44-113">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d44-114">-DefaultProfile</span></span>
<span data-ttu-id="a5d44-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d44-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="a5d44-116">-MigrateProjectName</span></span>
<span data-ttu-id="a5d44-117">Имя проекта миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d44-117">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d44-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5d44-119">Имя группы ресурсов Azure, в которую входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="a5d44-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5d44-120">-SubscriptionId</span></span>
<span data-ttu-id="a5d44-121">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="a5d44-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="a5d44-122">-Tool</span></span>
<span data-ttu-id="a5d44-123">Получает или настраивает регистрацию средства.</span><span class="sxs-lookup"><span data-stu-id="a5d44-123">Gets or sets the tool to be registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d44-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5d44-124">-Confirm</span></span>
<span data-ttu-id="a5d44-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a5d44-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d44-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d44-126">-WhatIf</span></span>
<span data-ttu-id="a5d44-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d44-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d44-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5d44-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d44-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d44-129">CommonParameters</span></span>
<span data-ttu-id="a5d44-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d44-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d44-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5d44-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d44-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d44-132">INPUTS</span></span>

## <span data-ttu-id="a5d44-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d44-133">OUTPUTS</span></span>

### <span data-ttu-id="a5d44-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5d44-134">System.Boolean</span></span>

## <span data-ttu-id="a5d44-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5d44-135">NOTES</span></span>

<span data-ttu-id="a5d44-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a5d44-136">ALIASES</span></span>

## <span data-ttu-id="a5d44-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5d44-137">RELATED LINKS</span></span>

