---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: 56891d1dae20f89289b9c2f72bf87bfeed7bd347
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978051"
---
# <span data-ttu-id="cafe5-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="cafe5-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="cafe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cafe5-102">SYNOPSIS</span></span>
<span data-ttu-id="cafe5-103">Удаляет прослушавщик группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cafe5-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="cafe5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cafe5-104">SYNTAX</span></span>

### <span data-ttu-id="cafe5-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cafe5-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cafe5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cafe5-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cafe5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cafe5-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cafe5-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="cafe5-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafe5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cafe5-109">DESCRIPTION</span></span>
<span data-ttu-id="cafe5-110">С Remove-AzAvailabilityGroupListener-за этого удаляется слушатель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cafe5-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="cafe5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cafe5-111">EXAMPLES</span></span>

### <span data-ttu-id="cafe5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cafe5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="cafe5-113">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="cafe5-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="cafe5-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="cafe5-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="cafe5-115">Удаляет прослушку Группы доступности AgListener01 в группе доступности AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="cafe5-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="cafe5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cafe5-116">PARAMETERS</span></span>

### <span data-ttu-id="cafe5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cafe5-117">-AsJob</span></span>
<span data-ttu-id="cafe5-118">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="cafe5-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="cafe5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafe5-119">-DefaultProfile</span></span>
<span data-ttu-id="cafe5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cafe5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cafe5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cafe5-121">-InputObject</span></span>
<span data-ttu-id="cafe5-122">Объект "Прослушивание группы доступности".</span><span class="sxs-lookup"><span data-stu-id="cafe5-122">Availability Group Listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cafe5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cafe5-123">-Name</span></span>
<span data-ttu-id="cafe5-124">Имя прослушавщика группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cafe5-124">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafe5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cafe5-125">-PassThru</span></span>
<span data-ttu-id="cafe5-126">Определяет, следует ли вы выводить удаленный ресурс в конце выполнения выполнения cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafe5-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="cafe5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cafe5-127">-ResourceGroupName</span></span>
<span data-ttu-id="cafe5-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cafe5-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafe5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cafe5-129">-ResourceId</span></span>
<span data-ttu-id="cafe5-130">ИД ресурса группы «Доступность»</span><span class="sxs-lookup"><span data-stu-id="cafe5-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafe5-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="cafe5-131">-SqlVMGroupName</span></span>
<span data-ttu-id="cafe5-132">SQL группы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cafe5-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafe5-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="cafe5-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="cafe5-134">SQL группа виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cafe5-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cafe5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cafe5-135">-Confirm</span></span>
<span data-ttu-id="cafe5-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafe5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafe5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafe5-137">-WhatIf</span></span>
<span data-ttu-id="cafe5-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafe5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cafe5-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cafe5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafe5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafe5-140">CommonParameters</span></span>
<span data-ttu-id="cafe5-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cafe5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafe5-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cafe5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafe5-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cafe5-143">INPUTS</span></span>

### <span data-ttu-id="cafe5-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="cafe5-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="cafe5-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cafe5-145">System.String</span></span>

### <span data-ttu-id="cafe5-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMaviree.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="cafe5-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="cafe5-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cafe5-147">OUTPUTS</span></span>

### <span data-ttu-id="cafe5-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMavire.Model.AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="cafe5-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="cafe5-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cafe5-149">NOTES</span></span>

## <span data-ttu-id="cafe5-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cafe5-150">RELATED LINKS</span></span>
