---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397548"
---
# <span data-ttu-id="b9b05-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="b9b05-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="b9b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9b05-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b05-103">Создание или обновление связи.</span><span class="sxs-lookup"><span data-stu-id="b9b05-103">Create or update an association.</span></span>

## <span data-ttu-id="b9b05-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9b05-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9b05-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9b05-105">DESCRIPTION</span></span>
<span data-ttu-id="b9b05-106">Создание или обновление связи.</span><span class="sxs-lookup"><span data-stu-id="b9b05-106">Create or update an association.</span></span>

## <span data-ttu-id="b9b05-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9b05-107">EXAMPLES</span></span>

### <span data-ttu-id="b9b05-108">Пример 1. Создание пользовательской связи поставщика</span><span class="sxs-lookup"><span data-stu-id="b9b05-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="b9b05-109">Создание пользовательской связи поставщика. Связанный целевой provioder должен быть правильно настроен с маршрутом для "associations"</span><span class="sxs-lookup"><span data-stu-id="b9b05-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="b9b05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9b05-110">PARAMETERS</span></span>

### <span data-ttu-id="b9b05-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9b05-111">-AsJob</span></span>
<span data-ttu-id="b9b05-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b9b05-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b9b05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b05-113">-DefaultProfile</span></span>
<span data-ttu-id="b9b05-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9b05-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9b05-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b9b05-115">-Name</span></span>
<span data-ttu-id="b9b05-116">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="b9b05-116">The name of the association.</span></span>

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

### <span data-ttu-id="b9b05-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9b05-117">-NoWait</span></span>
<span data-ttu-id="b9b05-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b9b05-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9b05-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="b9b05-119">-Scope</span></span>
<span data-ttu-id="b9b05-120">Область действия связи.</span><span class="sxs-lookup"><span data-stu-id="b9b05-120">The scope of the association.</span></span>
<span data-ttu-id="b9b05-121">Областью может быть любой допустимый экземпляр ресурса REST.</span><span class="sxs-lookup"><span data-stu-id="b9b05-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="b9b05-122">Например, для виртуального машинного ресурса используйте "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMaиоes/{vm-name}".</span><span class="sxs-lookup"><span data-stu-id="b9b05-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="b9b05-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b9b05-123">-TargetResourceId</span></span>
<span data-ttu-id="b9b05-124">Экземпляр ресурса REST целевого ресурса для этой связи.</span><span class="sxs-lookup"><span data-stu-id="b9b05-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="b9b05-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9b05-125">-Confirm</span></span>
<span data-ttu-id="b9b05-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b9b05-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b05-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b05-127">-WhatIf</span></span>
<span data-ttu-id="b9b05-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9b05-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b05-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b9b05-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b05-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b05-130">CommonParameters</span></span>
<span data-ttu-id="b9b05-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b05-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b05-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9b05-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b05-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9b05-133">INPUTS</span></span>

## <span data-ttu-id="b9b05-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9b05-134">OUTPUTS</span></span>

### <span data-ttu-id="b9b05-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="b9b05-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="b9b05-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9b05-136">NOTES</span></span>

<span data-ttu-id="b9b05-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b9b05-137">ALIASES</span></span>

## <span data-ttu-id="b9b05-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9b05-138">RELATED LINKS</span></span>

