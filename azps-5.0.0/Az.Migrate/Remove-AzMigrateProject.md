---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248628"
---
# <span data-ttu-id="e3ffa-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="e3ffa-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="e3ffa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ffa-103">Удалите проект миграции.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-103">Delete the migrate project.</span></span>
<span data-ttu-id="e3ffa-104">Удаление несуществующего проекта — это нерабочее действие.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e3ffa-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3ffa-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3ffa-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3ffa-106">DESCRIPTION</span></span>
<span data-ttu-id="e3ffa-107">Удалите проект миграции.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-107">Delete the migrate project.</span></span>
<span data-ttu-id="e3ffa-108">Удаление несуществующего проекта — это нерабочее действие.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e3ffa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3ffa-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ffa-110">Пример 1: Delete (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3ffa-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="e3ffa-111">Удалите проект миграции.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-111">Delete the migrate project.</span></span>
<span data-ttu-id="e3ffa-112">Удаление несуществующего проекта — это нерабочее действие.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="e3ffa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3ffa-113">PARAMETERS</span></span>

### <span data-ttu-id="e3ffa-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e3ffa-114">-AcceptLanguage</span></span>
<span data-ttu-id="e3ffa-115">Стандартный заголовок запроса.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-115">Standard request header.</span></span>
<span data-ttu-id="e3ffa-116">Используется службой для ответа на клиента на нужном языке.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="e3ffa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ffa-117">-DefaultProfile</span></span>
<span data-ttu-id="e3ffa-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ffa-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3ffa-119">-Name</span></span>
<span data-ttu-id="e3ffa-120">Имя проекта для миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ffa-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3ffa-121">-PassThru</span></span>
<span data-ttu-id="e3ffa-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e3ffa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ffa-123">-ResourceGroupName</span></span>
<span data-ttu-id="e3ffa-124">Имя группы ресурсов Azure, в состав которой входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="e3ffa-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3ffa-125">-SubscriptionId</span></span>
<span data-ttu-id="e3ffa-126">Идентификатор подписки Azure, в которой был создан проект миграции.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e3ffa-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3ffa-127">-Confirm</span></span>
<span data-ttu-id="e3ffa-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ffa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ffa-129">-WhatIf</span></span>
<span data-ttu-id="e3ffa-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ffa-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ffa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ffa-132">CommonParameters</span></span>
<span data-ttu-id="e3ffa-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3ffa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ffa-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3ffa-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ffa-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3ffa-135">INPUTS</span></span>

## <span data-ttu-id="e3ffa-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3ffa-136">OUTPUTS</span></span>

### <span data-ttu-id="e3ffa-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3ffa-137">System.Boolean</span></span>

## <span data-ttu-id="e3ffa-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3ffa-138">NOTES</span></span>

<span data-ttu-id="e3ffa-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e3ffa-139">ALIASES</span></span>

## <span data-ttu-id="e3ffa-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3ffa-140">RELATED LINKS</span></span>

