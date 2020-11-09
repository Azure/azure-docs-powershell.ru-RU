---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247349"
---
# <span data-ttu-id="e474a-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e474a-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="e474a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e474a-102">SYNOPSIS</span></span>
<span data-ttu-id="e474a-103">Запись конфигурации исправления</span><span class="sxs-lookup"><span data-stu-id="e474a-103">Patch configuration record</span></span>

## <span data-ttu-id="e474a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e474a-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e474a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e474a-105">DESCRIPTION</span></span>
<span data-ttu-id="e474a-106">Запись конфигурации обслуживания исправлений</span><span class="sxs-lookup"><span data-stu-id="e474a-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="e474a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e474a-107">EXAMPLES</span></span>

### <span data-ttu-id="e474a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e474a-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="e474a-109">Запись конфигурации обслуживания исправлений</span><span class="sxs-lookup"><span data-stu-id="e474a-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="e474a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e474a-110">PARAMETERS</span></span>

### <span data-ttu-id="e474a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e474a-111">-AsJob</span></span>
<span data-ttu-id="e474a-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e474a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e474a-113">-Configuration</span><span class="sxs-lookup"><span data-stu-id="e474a-113">-Configuration</span></span>
<span data-ttu-id="e474a-114">Конфигурация обслуживания, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="e474a-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e474a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e474a-115">-DefaultProfile</span></span>
<span data-ttu-id="e474a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e474a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e474a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e474a-117">-Name</span></span>
<span data-ttu-id="e474a-118">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e474a-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="e474a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e474a-119">-ResourceGroupName</span></span>
<span data-ttu-id="e474a-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e474a-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="e474a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e474a-121">-Confirm</span></span>
<span data-ttu-id="e474a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e474a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e474a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e474a-123">-WhatIf</span></span>
<span data-ttu-id="e474a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e474a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e474a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e474a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e474a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e474a-126">CommonParameters</span></span>
<span data-ttu-id="e474a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e474a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e474a-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e474a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e474a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e474a-129">INPUTS</span></span>

### <span data-ttu-id="e474a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e474a-130">System.String</span></span>

### <span data-ttu-id="e474a-131">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e474a-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e474a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e474a-132">OUTPUTS</span></span>

### <span data-ttu-id="e474a-133">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e474a-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="e474a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e474a-134">NOTES</span></span>

## <span data-ttu-id="e474a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e474a-135">RELATED LINKS</span></span>