---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242557"
---
# <span data-ttu-id="d26c5-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="d26c5-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="d26c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d26c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d26c5-103">Создание или обновление связи.</span><span class="sxs-lookup"><span data-stu-id="d26c5-103">Create or update an association.</span></span>

## <span data-ttu-id="d26c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d26c5-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d26c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d26c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d26c5-106">Создание или обновление связи.</span><span class="sxs-lookup"><span data-stu-id="d26c5-106">Create or update an association.</span></span>

## <span data-ttu-id="d26c5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d26c5-107">EXAMPLES</span></span>

### <span data-ttu-id="d26c5-108">Пример 1: Создание связи с настраиваемым поставщиком</span><span class="sxs-lookup"><span data-stu-id="d26c5-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="d26c5-109">Создание связи с настраиваемым поставщиком. соответствующие целевые provioder должны быть правильно настроены для маршрута "Associations"</span><span class="sxs-lookup"><span data-stu-id="d26c5-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="d26c5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d26c5-110">PARAMETERS</span></span>

### <span data-ttu-id="d26c5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d26c5-111">-AsJob</span></span>
<span data-ttu-id="d26c5-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d26c5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d26c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26c5-113">-DefaultProfile</span></span>
<span data-ttu-id="d26c5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d26c5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d26c5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d26c5-115">-Name</span></span>
<span data-ttu-id="d26c5-116">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="d26c5-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d26c5-117">-Wait</span><span class="sxs-lookup"><span data-stu-id="d26c5-117">-NoWait</span></span>
<span data-ttu-id="d26c5-118">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="d26c5-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d26c5-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="d26c5-119">-Scope</span></span>
<span data-ttu-id="d26c5-120">Область действия ассоциации.</span><span class="sxs-lookup"><span data-stu-id="d26c5-120">The scope of the association.</span></span>
<span data-ttu-id="d26c5-121">Область может быть любым допустимым экземпляром ресурса в оставшейся части.</span><span class="sxs-lookup"><span data-stu-id="d26c5-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="d26c5-122">Например, используйте "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}" для ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d26c5-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="d26c5-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d26c5-123">-TargetResourceId</span></span>
<span data-ttu-id="d26c5-124">Экземпляр ресурса ОСТАВШЕЙся целевого ресурса для этой связи.</span><span class="sxs-lookup"><span data-stu-id="d26c5-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="d26c5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d26c5-125">-Confirm</span></span>
<span data-ttu-id="d26c5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d26c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d26c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d26c5-127">-WhatIf</span></span>
<span data-ttu-id="d26c5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d26c5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d26c5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d26c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d26c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26c5-130">CommonParameters</span></span>
<span data-ttu-id="d26c5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d26c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26c5-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d26c5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26c5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d26c5-133">INPUTS</span></span>

## <span data-ttu-id="d26c5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d26c5-134">OUTPUTS</span></span>

### <span data-ttu-id="d26c5-135">Microsoft. Azure. PowerShell. командлеты. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="d26c5-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="d26c5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d26c5-136">NOTES</span></span>

<span data-ttu-id="d26c5-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d26c5-137">ALIASES</span></span>

## <span data-ttu-id="d26c5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d26c5-138">RELATED LINKS</span></span>

