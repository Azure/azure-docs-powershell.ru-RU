---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248633"
---
# <span data-ttu-id="49710-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="49710-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="49710-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49710-102">SYNOPSIS</span></span>
<span data-ttu-id="49710-103">Регистрация инструмента с проектом для миграции.</span><span class="sxs-lookup"><span data-stu-id="49710-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="49710-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49710-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="49710-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49710-105">DESCRIPTION</span></span>
<span data-ttu-id="49710-106">Регистрация инструмента с проектом для миграции.</span><span class="sxs-lookup"><span data-stu-id="49710-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="49710-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49710-107">EXAMPLES</span></span>

### <span data-ttu-id="49710-108">Пример 1: регистрация инструмента.</span><span class="sxs-lookup"><span data-stu-id="49710-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="49710-109">Регистрация инструмента с проектом для миграции.</span><span class="sxs-lookup"><span data-stu-id="49710-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="49710-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49710-110">PARAMETERS</span></span>

### <span data-ttu-id="49710-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="49710-111">-AcceptLanguage</span></span>
<span data-ttu-id="49710-112">Стандартный заголовок запроса.</span><span class="sxs-lookup"><span data-stu-id="49710-112">Standard request header.</span></span>
<span data-ttu-id="49710-113">Используется службой для ответа на клиента на нужном языке.</span><span class="sxs-lookup"><span data-stu-id="49710-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="49710-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49710-114">-DefaultProfile</span></span>
<span data-ttu-id="49710-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49710-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49710-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="49710-116">-MigrateProjectName</span></span>
<span data-ttu-id="49710-117">Имя проекта для миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="49710-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="49710-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49710-118">-ResourceGroupName</span></span>
<span data-ttu-id="49710-119">Имя группы ресурсов Azure, в состав которой входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="49710-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="49710-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49710-120">-SubscriptionId</span></span>
<span data-ttu-id="49710-121">Идентификатор подписки Azure, в которой был создан проект миграции.</span><span class="sxs-lookup"><span data-stu-id="49710-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="49710-122">-Инструмент</span><span class="sxs-lookup"><span data-stu-id="49710-122">-Tool</span></span>
<span data-ttu-id="49710-123">Возвращает или задает средство, которое нужно зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="49710-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="49710-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49710-124">-Confirm</span></span>
<span data-ttu-id="49710-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49710-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49710-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49710-126">-WhatIf</span></span>
<span data-ttu-id="49710-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49710-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49710-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49710-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49710-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49710-129">CommonParameters</span></span>
<span data-ttu-id="49710-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49710-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49710-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49710-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49710-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49710-132">INPUTS</span></span>

## <span data-ttu-id="49710-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49710-133">OUTPUTS</span></span>

### <span data-ttu-id="49710-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49710-134">System.Boolean</span></span>

## <span data-ttu-id="49710-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="49710-135">NOTES</span></span>

<span data-ttu-id="49710-136">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="49710-136">ALIASES</span></span>

## <span data-ttu-id="49710-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49710-137">RELATED LINKS</span></span>

