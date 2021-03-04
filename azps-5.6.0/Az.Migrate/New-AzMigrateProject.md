---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982691"
---
# <span data-ttu-id="270f5-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="270f5-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="270f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270f5-102">SYNOPSIS</span></span>
<span data-ttu-id="270f5-103">Создает новый проект миграции.</span><span class="sxs-lookup"><span data-stu-id="270f5-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="270f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="270f5-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="270f5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="270f5-105">DESCRIPTION</span></span>
<span data-ttu-id="270f5-106">Создает новый проект миграции.</span><span class="sxs-lookup"><span data-stu-id="270f5-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="270f5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="270f5-107">EXAMPLES</span></span>

### <span data-ttu-id="270f5-108">Пример 1. Создание (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="270f5-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="270f5-109">Способ создания проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="270f5-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="270f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="270f5-110">PARAMETERS</span></span>

### <span data-ttu-id="270f5-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="270f5-111">-ETag</span></span>
<span data-ttu-id="270f5-112">Указывает имя компьютера VMWARE.</span><span class="sxs-lookup"><span data-stu-id="270f5-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="270f5-113">-Location</span><span class="sxs-lookup"><span data-stu-id="270f5-113">-Location</span></span>
<span data-ttu-id="270f5-114">Указывает имя компьютера VMWARE.</span><span class="sxs-lookup"><span data-stu-id="270f5-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="270f5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="270f5-115">-Name</span></span>
<span data-ttu-id="270f5-116">Указывает имя переносимого проекта.</span><span class="sxs-lookup"><span data-stu-id="270f5-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="270f5-117">-Свойство</span><span class="sxs-lookup"><span data-stu-id="270f5-117">-Property</span></span>
<span data-ttu-id="270f5-118">Определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="270f5-118">Specifies the project properties.</span></span>
<span data-ttu-id="270f5-119">Чтобы построить таблицу, см. раздел "ЗАМЕТКИ" для свойств и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="270f5-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="270f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="270f5-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="270f5-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="270f5-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="270f5-122">-SubscriptionId</span></span>
<span data-ttu-id="270f5-123">Определяет ид подписки.</span><span class="sxs-lookup"><span data-stu-id="270f5-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="270f5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="270f5-124">-Confirm</span></span>
<span data-ttu-id="270f5-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="270f5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270f5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270f5-126">-WhatIf</span></span>
<span data-ttu-id="270f5-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270f5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="270f5-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="270f5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270f5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270f5-129">CommonParameters</span></span>
<span data-ttu-id="270f5-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270f5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270f5-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="270f5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270f5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="270f5-132">INPUTS</span></span>

## <span data-ttu-id="270f5-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="270f5-133">OUTPUTS</span></span>

## <span data-ttu-id="270f5-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="270f5-134">NOTES</span></span>

<span data-ttu-id="270f5-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="270f5-135">ALIASES</span></span>

<span data-ttu-id="270f5-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="270f5-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="270f5-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="270f5-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="270f5-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="270f5-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="270f5-139">СВОЙСТВО: <IMigrateProjectProperties> определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="270f5-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="270f5-140">`[ProvisioningState <ProvisioningState?>]`: подготовка проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="270f5-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="270f5-141">`[RegisteredTool <String[]>]`: получает или задает список средств, зарегистрированных в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="270f5-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="270f5-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="270f5-142">RELATED LINKS</span></span>

