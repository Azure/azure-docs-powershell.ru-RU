---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417079"
---
# <span data-ttu-id="7bec9-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7bec9-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="7bec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bec9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bec9-103">Создает новый проект миграции.</span><span class="sxs-lookup"><span data-stu-id="7bec9-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="7bec9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7bec9-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7bec9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bec9-105">DESCRIPTION</span></span>
<span data-ttu-id="7bec9-106">Создает новый проект миграции.</span><span class="sxs-lookup"><span data-stu-id="7bec9-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="7bec9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7bec9-107">EXAMPLES</span></span>

### <span data-ttu-id="7bec9-108">Пример 1. Создание (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7bec9-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="7bec9-109">Способ создания проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="7bec9-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="7bec9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bec9-110">PARAMETERS</span></span>

### <span data-ttu-id="7bec9-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="7bec9-111">-ETag</span></span>
<span data-ttu-id="7bec9-112">Указывает имя компьютера VMWARE.</span><span class="sxs-lookup"><span data-stu-id="7bec9-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="7bec9-113">-Location</span><span class="sxs-lookup"><span data-stu-id="7bec9-113">-Location</span></span>
<span data-ttu-id="7bec9-114">Указывает имя компьютера VMWARE.</span><span class="sxs-lookup"><span data-stu-id="7bec9-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="7bec9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7bec9-115">-Name</span></span>
<span data-ttu-id="7bec9-116">Указывает имя переносимого проекта.</span><span class="sxs-lookup"><span data-stu-id="7bec9-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="7bec9-117">-Свойство</span><span class="sxs-lookup"><span data-stu-id="7bec9-117">-Property</span></span>
<span data-ttu-id="7bec9-118">Определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="7bec9-118">Specifies the project properties.</span></span>
<span data-ttu-id="7bec9-119">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="7bec9-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="7bec9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bec9-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bec9-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7bec9-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="7bec9-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bec9-122">-SubscriptionId</span></span>
<span data-ttu-id="7bec9-123">Определяет ид подписки.</span><span class="sxs-lookup"><span data-stu-id="7bec9-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="7bec9-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bec9-124">-Confirm</span></span>
<span data-ttu-id="7bec9-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bec9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bec9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bec9-126">-WhatIf</span></span>
<span data-ttu-id="7bec9-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bec9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bec9-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7bec9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bec9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bec9-129">CommonParameters</span></span>
<span data-ttu-id="7bec9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bec9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bec9-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bec9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bec9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bec9-132">INPUTS</span></span>

## <span data-ttu-id="7bec9-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7bec9-133">OUTPUTS</span></span>

## <span data-ttu-id="7bec9-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7bec9-134">NOTES</span></span>

<span data-ttu-id="7bec9-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7bec9-135">ALIASES</span></span>

<span data-ttu-id="7bec9-136">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7bec9-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7bec9-137">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7bec9-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7bec9-138">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7bec9-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7bec9-139">СВОЙСТВО: <IMigrateProjectProperties> определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="7bec9-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="7bec9-140">`[ProvisioningState <ProvisioningState?>]`: подготовка проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="7bec9-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="7bec9-141">`[RegisteredTool <String[]>]`: получает или задает список средств, зарегистрированных в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="7bec9-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="7bec9-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bec9-142">RELATED LINKS</span></span>

