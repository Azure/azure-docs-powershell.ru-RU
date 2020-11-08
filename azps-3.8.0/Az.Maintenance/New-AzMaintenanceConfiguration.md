---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074220"
---
# <span data-ttu-id="bc358-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc358-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="bc358-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc358-102">SYNOPSIS</span></span>
<span data-ttu-id="bc358-103">Создание или обновление записи конфигурации</span><span class="sxs-lookup"><span data-stu-id="bc358-103">Create or Update configuration record</span></span>

## <span data-ttu-id="bc358-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc358-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc358-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc358-105">DESCRIPTION</span></span>
<span data-ttu-id="bc358-106">Создание или обновление записи конфигурации</span><span class="sxs-lookup"><span data-stu-id="bc358-106">Create or Update configuration record</span></span>

## <span data-ttu-id="bc358-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc358-107">EXAMPLES</span></span>

### <span data-ttu-id="bc358-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc358-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="bc358-109">Создание конфигурации обслуживания с узлом области</span><span class="sxs-lookup"><span data-stu-id="bc358-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="bc358-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc358-110">PARAMETERS</span></span>

### <span data-ttu-id="bc358-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc358-111">-AsJob</span></span>
<span data-ttu-id="bc358-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bc358-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc358-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc358-113">-DefaultProfile</span></span>
<span data-ttu-id="bc358-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc358-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc358-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="bc358-115">-ExtensionProperty</span></span>
<span data-ttu-id="bc358-116">Свойства расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc358-116">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc358-117">-Location</span><span class="sxs-lookup"><span data-stu-id="bc358-117">-Location</span></span>
<span data-ttu-id="bc358-118">Расположение конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="bc358-118">The maintenance configuration location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc358-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="bc358-119">-MaintenanceScope</span></span>
<span data-ttu-id="bc358-120">Область обслуживания.</span><span class="sxs-lookup"><span data-stu-id="bc358-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="bc358-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc358-121">-Name</span></span>
<span data-ttu-id="bc358-122">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="bc358-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="bc358-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc358-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc358-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc358-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="bc358-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="bc358-125">-Tag</span></span>
<span data-ttu-id="bc358-126">Теги ARM.</span><span class="sxs-lookup"><span data-stu-id="bc358-126">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc358-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc358-127">-Confirm</span></span>
<span data-ttu-id="bc358-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc358-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc358-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc358-129">-WhatIf</span></span>
<span data-ttu-id="bc358-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc358-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc358-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc358-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc358-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc358-132">CommonParameters</span></span>
<span data-ttu-id="bc358-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc358-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc358-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc358-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc358-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc358-135">INPUTS</span></span>

### <span data-ttu-id="bc358-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bc358-136">System.String</span></span>

## <span data-ttu-id="bc358-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc358-137">OUTPUTS</span></span>

### <span data-ttu-id="bc358-138">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc358-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="bc358-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc358-139">NOTES</span></span>

## <span data-ttu-id="bc358-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc358-140">RELATED LINKS</span></span>
