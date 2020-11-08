---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247699"
---
# <span data-ttu-id="4b4f8-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="4b4f8-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="4b4f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4f8-103">Применение обновлений для обслуживания к ресурсу</span><span class="sxs-lookup"><span data-stu-id="4b4f8-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="4b4f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b4f8-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b4f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b4f8-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4f8-106">Применение обновлений для обслуживания к ресурсу</span><span class="sxs-lookup"><span data-stu-id="4b4f8-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="4b4f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b4f8-107">EXAMPLES</span></span>

### <span data-ttu-id="4b4f8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b4f8-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="4b4f8-109">Применение обновлений для обслуживания к ресурсу</span><span class="sxs-lookup"><span data-stu-id="4b4f8-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="4b4f8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b4f8-110">PARAMETERS</span></span>

### <span data-ttu-id="4b4f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b4f8-111">-AsJob</span></span>
<span data-ttu-id="4b4f8-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4b4f8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b4f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4f8-113">-DefaultProfile</span></span>
<span data-ttu-id="4b4f8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b4f8-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4b4f8-115">-ProviderName</span></span>
<span data-ttu-id="4b4f8-116">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="4b4f8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4f8-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b4f8-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="4b4f8-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4b4f8-119">-ResourceName</span></span>
<span data-ttu-id="4b4f8-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4f8-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="4b4f8-121">-ResourceParentName</span></span>
<span data-ttu-id="4b4f8-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4f8-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="4b4f8-123">-ResourceParentType</span></span>
<span data-ttu-id="4b4f8-124">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4f8-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4b4f8-125">-ResourceType</span></span>
<span data-ttu-id="4b4f8-126">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-126">The resource type.</span></span>

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

### <span data-ttu-id="4b4f8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b4f8-127">-Confirm</span></span>
<span data-ttu-id="4b4f8-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4f8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4f8-129">-WhatIf</span></span>
<span data-ttu-id="4b4f8-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b4f8-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4f8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4f8-132">CommonParameters</span></span>
<span data-ttu-id="4b4f8-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b4f8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4f8-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b4f8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4f8-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b4f8-135">INPUTS</span></span>

### <span data-ttu-id="4b4f8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4b4f8-136">System.String</span></span>

## <span data-ttu-id="4b4f8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b4f8-137">OUTPUTS</span></span>

### <span data-ttu-id="4b4f8-138">Microsoft. Azure. Commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="4b4f8-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="4b4f8-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b4f8-139">NOTES</span></span>

## <span data-ttu-id="4b4f8-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b4f8-140">RELATED LINKS</span></span>
