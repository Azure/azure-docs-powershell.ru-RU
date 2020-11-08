---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248864"
---
# <span data-ttu-id="091c2-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="091c2-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="091c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="091c2-102">SYNOPSIS</span></span>
<span data-ttu-id="091c2-103">Создание нового проекта для миграции.</span><span class="sxs-lookup"><span data-stu-id="091c2-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="091c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="091c2-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="091c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="091c2-105">DESCRIPTION</span></span>
<span data-ttu-id="091c2-106">Создание нового проекта для миграции.</span><span class="sxs-lookup"><span data-stu-id="091c2-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="091c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="091c2-107">EXAMPLES</span></span>

### <span data-ttu-id="091c2-108">Пример 1: Create (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="091c2-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="091c2-109">Метод для создания нового проекта миграции.</span><span class="sxs-lookup"><span data-stu-id="091c2-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="091c2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="091c2-110">PARAMETERS</span></span>

### <span data-ttu-id="091c2-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="091c2-111">-ETag</span></span>
<span data-ttu-id="091c2-112">Указывает имя компьютера VMware.</span><span class="sxs-lookup"><span data-stu-id="091c2-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="091c2-113">-Location</span><span class="sxs-lookup"><span data-stu-id="091c2-113">-Location</span></span>
<span data-ttu-id="091c2-114">Указывает имя компьютера VMware.</span><span class="sxs-lookup"><span data-stu-id="091c2-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="091c2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="091c2-115">-Name</span></span>
<span data-ttu-id="091c2-116">Указывает имя переносимого проекта.</span><span class="sxs-lookup"><span data-stu-id="091c2-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="091c2-117">-Property</span><span class="sxs-lookup"><span data-stu-id="091c2-117">-Property</span></span>
<span data-ttu-id="091c2-118">Задает свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="091c2-118">Specifies the project properties.</span></span>
<span data-ttu-id="091c2-119">Для конструирования ознакомьтесь с разделом "Заметки" для свойств свойств и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="091c2-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="091c2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="091c2-120">-ResourceGroupName</span></span>
<span data-ttu-id="091c2-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="091c2-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="091c2-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="091c2-122">-SubscriptionId</span></span>
<span data-ttu-id="091c2-123">Указывает идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="091c2-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="091c2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="091c2-124">-Confirm</span></span>
<span data-ttu-id="091c2-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="091c2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="091c2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091c2-126">-WhatIf</span></span>
<span data-ttu-id="091c2-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="091c2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="091c2-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="091c2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="091c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091c2-129">CommonParameters</span></span>
<span data-ttu-id="091c2-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="091c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091c2-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="091c2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091c2-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="091c2-132">INPUTS</span></span>

## <span data-ttu-id="091c2-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="091c2-133">OUTPUTS</span></span>

## <span data-ttu-id="091c2-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="091c2-134">NOTES</span></span>

<span data-ttu-id="091c2-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="091c2-135">ALIASES</span></span>

<span data-ttu-id="091c2-136">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="091c2-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="091c2-137">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="091c2-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="091c2-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="091c2-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="091c2-139">Свойство <IMigrateProjectProperties> : определяет свойства проекта.</span><span class="sxs-lookup"><span data-stu-id="091c2-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="091c2-140">`[ProvisioningState <ProvisioningState?>]`: Состояние подготовки проекта для миграции.</span><span class="sxs-lookup"><span data-stu-id="091c2-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="091c2-141">`[RegisteredTool <String[]>]`: Получает или задает список инструментов, зарегистрированных в проекте миграции.</span><span class="sxs-lookup"><span data-stu-id="091c2-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="091c2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="091c2-142">RELATED LINKS</span></span>

