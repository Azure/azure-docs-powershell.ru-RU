---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: 60cc9b5b537c1d8e46f5bae56d93b33fa04f6c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976776"
---
# <span data-ttu-id="77ec1-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="77ec1-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="77ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="77ec1-103">Регистрирует средство в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="77ec1-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="77ec1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77ec1-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="77ec1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="77ec1-106">Регистрирует средство в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="77ec1-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="77ec1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="77ec1-108">Пример 1. Инструмент REgister.</span><span class="sxs-lookup"><span data-stu-id="77ec1-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="77ec1-109">Регистрирует средство в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="77ec1-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="77ec1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="77ec1-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="77ec1-111">-AcceptLanguage</span></span>
<span data-ttu-id="77ec1-112">Стандартный заметив запроса.</span><span class="sxs-lookup"><span data-stu-id="77ec1-112">Standard request header.</span></span>
<span data-ttu-id="77ec1-113">Используется службой для ответа на клиент на соответствующем языке.</span><span class="sxs-lookup"><span data-stu-id="77ec1-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="77ec1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ec1-114">-DefaultProfile</span></span>
<span data-ttu-id="77ec1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77ec1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77ec1-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="77ec1-116">-MigrateProjectName</span></span>
<span data-ttu-id="77ec1-117">Имя проекта миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="77ec1-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="77ec1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ec1-118">-ResourceGroupName</span></span>
<span data-ttu-id="77ec1-119">Имя группы ресурсов Azure, в которую входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="77ec1-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="77ec1-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77ec1-120">-SubscriptionId</span></span>
<span data-ttu-id="77ec1-121">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="77ec1-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="77ec1-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="77ec1-122">-Tool</span></span>
<span data-ttu-id="77ec1-123">Получает или настраивает регистрацию средства.</span><span class="sxs-lookup"><span data-stu-id="77ec1-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="77ec1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77ec1-124">-Confirm</span></span>
<span data-ttu-id="77ec1-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ec1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77ec1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77ec1-126">-WhatIf</span></span>
<span data-ttu-id="77ec1-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77ec1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77ec1-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="77ec1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77ec1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ec1-129">CommonParameters</span></span>
<span data-ttu-id="77ec1-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77ec1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ec1-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77ec1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ec1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77ec1-132">INPUTS</span></span>

## <span data-ttu-id="77ec1-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77ec1-133">OUTPUTS</span></span>

### <span data-ttu-id="77ec1-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77ec1-134">System.Boolean</span></span>

## <span data-ttu-id="77ec1-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77ec1-135">NOTES</span></span>

<span data-ttu-id="77ec1-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="77ec1-136">ALIASES</span></span>

## <span data-ttu-id="77ec1-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77ec1-137">RELATED LINKS</span></span>

