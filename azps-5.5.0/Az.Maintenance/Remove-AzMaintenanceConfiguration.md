---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219204"
---
# <span data-ttu-id="953f2-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="953f2-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="953f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="953f2-102">SYNOPSIS</span></span>
<span data-ttu-id="953f2-103">Удаление записи конфигурации</span><span class="sxs-lookup"><span data-stu-id="953f2-103">Delete Configuration record</span></span>

## <span data-ttu-id="953f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="953f2-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="953f2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="953f2-105">DESCRIPTION</span></span>
<span data-ttu-id="953f2-106">Удаление записи конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="953f2-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="953f2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="953f2-107">EXAMPLES</span></span>

### <span data-ttu-id="953f2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="953f2-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="953f2-109">Удаление записи конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="953f2-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="953f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="953f2-110">PARAMETERS</span></span>

### <span data-ttu-id="953f2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="953f2-111">-AsJob</span></span>
<span data-ttu-id="953f2-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="953f2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="953f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953f2-113">-DefaultProfile</span></span>
<span data-ttu-id="953f2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="953f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953f2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="953f2-115">-Force</span></span>
<span data-ttu-id="953f2-116">Принудительное удаление без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="953f2-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="953f2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="953f2-117">-Name</span></span>
<span data-ttu-id="953f2-118">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="953f2-118">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953f2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="953f2-119">-PassThru</span></span>
<span data-ttu-id="953f2-120">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="953f2-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="953f2-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="953f2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="953f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="953f2-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="953f2-123">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953f2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="953f2-124">-Confirm</span></span>
<span data-ttu-id="953f2-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="953f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953f2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953f2-126">-WhatIf</span></span>
<span data-ttu-id="953f2-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="953f2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953f2-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="953f2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="953f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953f2-129">CommonParameters</span></span>
<span data-ttu-id="953f2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953f2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="953f2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953f2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="953f2-132">INPUTS</span></span>

### <span data-ttu-id="953f2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="953f2-133">System.String</span></span>

## <span data-ttu-id="953f2-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="953f2-134">OUTPUTS</span></span>

### <span data-ttu-id="953f2-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="953f2-135">System.Boolean</span></span>

## <span data-ttu-id="953f2-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="953f2-136">NOTES</span></span>

## <span data-ttu-id="953f2-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="953f2-137">RELATED LINKS</span></span>
