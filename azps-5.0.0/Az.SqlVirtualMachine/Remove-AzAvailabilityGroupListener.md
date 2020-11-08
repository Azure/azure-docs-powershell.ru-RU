---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/remove-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Remove-AzAvailabilityGroupListener.md
ms.openlocfilehash: d147fcd53b27031949bf51a33a59a9db86687d57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245644"
---
# <span data-ttu-id="64e29-101">Remove-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="64e29-101">Remove-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="64e29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64e29-102">SYNOPSIS</span></span>
<span data-ttu-id="64e29-103">Удаление прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="64e29-103">Deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="64e29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64e29-104">SYNTAX</span></span>

### <span data-ttu-id="64e29-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64e29-105">Name (Default)</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-ResourceGroupName] <String>
 [-SqlVMGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64e29-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="64e29-106">InputObject</span></span>
```
Remove-AzAvailabilityGroupListener [-InputObject] <AzureAvailabilityGroupListenerModel> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e29-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="64e29-107">ResourceId</span></span>
```
Remove-AzAvailabilityGroupListener [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64e29-108">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="64e29-108">SqlVmGroupObject</span></span>
```
Remove-AzAvailabilityGroupListener [-AsJob] [-PassThru] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64e29-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e29-109">DESCRIPTION</span></span>
<span data-ttu-id="64e29-110">Командлет Remove-AzAvailabilityGroupListener Удаляет прослушиватель группы доступности.</span><span class="sxs-lookup"><span data-stu-id="64e29-110">The Remove-AzAvailabilityGroupListener cmdlet deletes an Availability Group Listener.</span></span>

## <span data-ttu-id="64e29-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64e29-111">EXAMPLES</span></span>

### <span data-ttu-id="64e29-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64e29-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="64e29-113">Name ResourceGroupName имя_группы AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="64e29-113">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="64e29-114">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="64e29-114">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="64e29-115">Удаляет AgListener01 прослушивателя группы доступности в группе доступности AvailabilityGroup01.</span><span class="sxs-lookup"><span data-stu-id="64e29-115">Deletes the Availability Group Listener AgListener01 in the Availability Group AvailabilityGroup01.</span></span>

## <span data-ttu-id="64e29-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64e29-116">PARAMETERS</span></span>

### <span data-ttu-id="64e29-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64e29-117">-AsJob</span></span>
<span data-ttu-id="64e29-118">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="64e29-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="64e29-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64e29-119">-DefaultProfile</span></span>
<span data-ttu-id="64e29-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64e29-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64e29-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64e29-121">-InputObject</span></span>
<span data-ttu-id="64e29-122">Объект прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="64e29-122">Availability Group Listener object.</span></span>

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

### <span data-ttu-id="64e29-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64e29-123">-Name</span></span>
<span data-ttu-id="64e29-124">Имя прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="64e29-124">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="64e29-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64e29-125">-PassThru</span></span>
<span data-ttu-id="64e29-126">Указывает, следует ли выводить удаленный ресурс при завершении выполнения командлета.</span><span class="sxs-lookup"><span data-stu-id="64e29-126">Specifies whether to output the deleted resource at end of cmdlet execution.</span></span>

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

### <span data-ttu-id="64e29-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64e29-127">-ResourceGroupName</span></span>
<span data-ttu-id="64e29-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64e29-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="64e29-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64e29-129">-ResourceId</span></span>
<span data-ttu-id="64e29-130">Идентификатор ресурса прослушивателя группы доступности</span><span class="sxs-lookup"><span data-stu-id="64e29-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="64e29-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="64e29-131">-SqlVMGroupName</span></span>
<span data-ttu-id="64e29-132">Имя группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="64e29-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="64e29-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="64e29-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="64e29-134">Объект группы виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="64e29-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="64e29-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64e29-135">-Confirm</span></span>
<span data-ttu-id="64e29-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64e29-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64e29-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64e29-137">-WhatIf</span></span>
<span data-ttu-id="64e29-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64e29-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64e29-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64e29-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64e29-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64e29-140">CommonParameters</span></span>
<span data-ttu-id="64e29-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64e29-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64e29-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64e29-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64e29-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64e29-143">INPUTS</span></span>

### <span data-ttu-id="64e29-144">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="64e29-144">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

### <span data-ttu-id="64e29-145">System. String</span><span class="sxs-lookup"><span data-stu-id="64e29-145">System.String</span></span>

### <span data-ttu-id="64e29-146">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="64e29-146">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="64e29-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64e29-147">OUTPUTS</span></span>

### <span data-ttu-id="64e29-148">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="64e29-148">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="64e29-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="64e29-149">NOTES</span></span>

## <span data-ttu-id="64e29-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64e29-150">RELATED LINKS</span></span>
