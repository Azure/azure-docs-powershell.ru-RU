---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237396"
---
# <span data-ttu-id="5fb19-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="5fb19-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="5fb19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb19-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb19-103">Создает новый проект миграции.</span><span class="sxs-lookup"><span data-stu-id="5fb19-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="5fb19-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fb19-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fb19-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fb19-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb19-106">Создает новый проект миграции.</span><span class="sxs-lookup"><span data-stu-id="5fb19-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="5fb19-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fb19-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb19-108">Пример 1. Создание (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fb19-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="5fb19-109">Способ создания проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="5fb19-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="5fb19-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fb19-110">PARAMETERS</span></span>

### <span data-ttu-id="5fb19-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="5fb19-111">-ETag</span></span>
<span data-ttu-id="5fb19-112">Указывает имя компьютера VMWARE.</span><span class="sxs-lookup"><span data-stu-id="5fb19-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="5fb19-113">-Location</span><span class="sxs-lookup"><span data-stu-id="5fb19-113">-Location</span></span>
<span data-ttu-id="5fb19-114">Указывает имя компьютера VMWARE.</span><span class="sxs-lookup"><span data-stu-id="5fb19-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="5fb19-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5fb19-115">-Name</span></span>
<span data-ttu-id="5fb19-116">Указывает имя переносимого проекта.</span><span class="sxs-lookup"><span data-stu-id="5fb19-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="5fb19-117">-Свойство</span><span class="sxs-lookup"><span data-stu-id="5fb19-117">-Property</span></span>
<span data-ttu-id="5fb19-118">Определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="5fb19-118">Specifies the project properties.</span></span>
<span data-ttu-id="5fb19-119">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5fb19-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb19-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb19-120">-ResourceGroupName</span></span>
<span data-ttu-id="5fb19-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fb19-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="5fb19-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fb19-122">-SubscriptionId</span></span>
<span data-ttu-id="5fb19-123">Определяет ид подписки.</span><span class="sxs-lookup"><span data-stu-id="5fb19-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="5fb19-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fb19-124">-Confirm</span></span>
<span data-ttu-id="5fb19-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5fb19-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb19-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb19-126">-WhatIf</span></span>
<span data-ttu-id="5fb19-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fb19-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb19-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5fb19-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb19-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb19-129">CommonParameters</span></span>
<span data-ttu-id="5fb19-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb19-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb19-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fb19-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb19-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fb19-132">INPUTS</span></span>

## <span data-ttu-id="5fb19-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fb19-133">OUTPUTS</span></span>

## <span data-ttu-id="5fb19-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fb19-134">NOTES</span></span>

<span data-ttu-id="5fb19-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5fb19-135">ALIASES</span></span>

<span data-ttu-id="5fb19-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5fb19-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fb19-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5fb19-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fb19-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fb19-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fb19-139">СВОЙСТВО: <IMigrateProjectProperties> определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="5fb19-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="5fb19-140">`[ProvisioningState <ProvisioningState?>]`: подготовка проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="5fb19-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="5fb19-141">`[RegisteredTool <String[]>]`: получает или задает список средств, зарегистрированных в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="5fb19-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="5fb19-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fb19-142">RELATED LINKS</span></span>

