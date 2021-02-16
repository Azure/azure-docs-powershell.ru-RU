---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219132"
---
# <span data-ttu-id="82604-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="82604-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="82604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82604-102">SYNOPSIS</span></span>
<span data-ttu-id="82604-103">Удалите проект миграции.</span><span class="sxs-lookup"><span data-stu-id="82604-103">Delete the migrate project.</span></span>
<span data-ttu-id="82604-104">Удаление несуществующего проекта не является операцией.</span><span class="sxs-lookup"><span data-stu-id="82604-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="82604-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82604-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82604-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82604-106">DESCRIPTION</span></span>
<span data-ttu-id="82604-107">Удалите проект миграции.</span><span class="sxs-lookup"><span data-stu-id="82604-107">Delete the migrate project.</span></span>
<span data-ttu-id="82604-108">Удаление несуществующего проекта не является операцией.</span><span class="sxs-lookup"><span data-stu-id="82604-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="82604-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82604-109">EXAMPLES</span></span>

### <span data-ttu-id="82604-110">Пример 1. Удаление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82604-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="82604-111">Удалите проект миграции.</span><span class="sxs-lookup"><span data-stu-id="82604-111">Delete the migrate project.</span></span>
<span data-ttu-id="82604-112">Удаление несуществующего проекта не является операцией.</span><span class="sxs-lookup"><span data-stu-id="82604-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="82604-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82604-113">PARAMETERS</span></span>

### <span data-ttu-id="82604-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="82604-114">-AcceptLanguage</span></span>
<span data-ttu-id="82604-115">Стандартный заметив запроса.</span><span class="sxs-lookup"><span data-stu-id="82604-115">Standard request header.</span></span>
<span data-ttu-id="82604-116">Используется службой для ответа на клиент на соответствующем языке.</span><span class="sxs-lookup"><span data-stu-id="82604-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="82604-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82604-117">-DefaultProfile</span></span>
<span data-ttu-id="82604-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82604-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82604-119">-Name</span><span class="sxs-lookup"><span data-stu-id="82604-119">-Name</span></span>
<span data-ttu-id="82604-120">Имя проекта миграции Azure.</span><span class="sxs-lookup"><span data-stu-id="82604-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="82604-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82604-121">-PassThru</span></span>
<span data-ttu-id="82604-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="82604-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="82604-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82604-123">-ResourceGroupName</span></span>
<span data-ttu-id="82604-124">Имя группы ресурсов Azure, в которую входит переносимый проект.</span><span class="sxs-lookup"><span data-stu-id="82604-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="82604-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82604-125">-SubscriptionId</span></span>
<span data-ttu-id="82604-126">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="82604-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="82604-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82604-127">-Confirm</span></span>
<span data-ttu-id="82604-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82604-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82604-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82604-129">-WhatIf</span></span>
<span data-ttu-id="82604-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82604-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82604-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82604-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82604-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82604-132">CommonParameters</span></span>
<span data-ttu-id="82604-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82604-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82604-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82604-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82604-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82604-135">INPUTS</span></span>

## <span data-ttu-id="82604-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82604-136">OUTPUTS</span></span>

### <span data-ttu-id="82604-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82604-137">System.Boolean</span></span>

## <span data-ttu-id="82604-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82604-138">NOTES</span></span>

<span data-ttu-id="82604-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="82604-139">ALIASES</span></span>

## <span data-ttu-id="82604-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82604-140">RELATED LINKS</span></span>

