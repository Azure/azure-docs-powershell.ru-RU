---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssVM.md
ms.openlocfilehash: 32e04fb16d0e3360abb22177e453d5d629dbb098
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074607"
---
# <span data-ttu-id="eb741-101">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="eb741-101">Set-AzVmssVM</span></span>

## <span data-ttu-id="eb741-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb741-102">SYNOPSIS</span></span>
<span data-ttu-id="eb741-103">Изменяет состояние экземпляра VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb741-103">Modifies the state of a VMSS instance.</span></span>

## <span data-ttu-id="eb741-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb741-104">SYNTAX</span></span>

### <span data-ttu-id="eb741-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb741-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb741-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="eb741-106">FriendMethod</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb741-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="eb741-107">RedeployMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb741-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="eb741-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb741-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb741-109">DESCRIPTION</span></span>
<span data-ttu-id="eb741-110">Командлет **Set-AzVmssVM** изменяет состояние экземпляра набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="eb741-110">The **Set-AzVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="eb741-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb741-111">EXAMPLES</span></span>

## <span data-ttu-id="eb741-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb741-112">PARAMETERS</span></span>

### <span data-ttu-id="eb741-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb741-113">-AsJob</span></span>
<span data-ttu-id="eb741-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eb741-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb741-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb741-115">-DefaultProfile</span></span>
<span data-ttu-id="eb741-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb741-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb741-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="eb741-117">-InstanceId</span></span>
<span data-ttu-id="eb741-118">Указывает идентификатор экземпляра VMSS, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="eb741-118">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

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

### <span data-ttu-id="eb741-119">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="eb741-119">-PerformMaintenance</span></span>
<span data-ttu-id="eb741-120">Указывает на то, что этот командлет выполняет обслуживание виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb741-120">Indicates that this cmdlet performs maintenance on a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb741-121">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="eb741-121">-Redeploy</span></span>
<span data-ttu-id="eb741-122">Указывает на то, что этот командлет повторно развертывает виртуальную машину в VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb741-122">Indicates that this cmdlet redeploys a virtual machine in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb741-123">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="eb741-123">-Reimage</span></span>
<span data-ttu-id="eb741-124">Указывает на то, что этот командлет переобразировать экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb741-124">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb741-125">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="eb741-125">-ReimageAll</span></span>
<span data-ttu-id="eb741-126">Указывает, что командлет переобразует все диски в экземпляре VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb741-126">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb741-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb741-127">-ResourceGroupName</span></span>
<span data-ttu-id="eb741-128">Указывает имя группы ресурсов, которая содержит экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="eb741-128">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="eb741-129">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="eb741-129">-VMScaleSetName</span></span>
<span data-ttu-id="eb741-130">Указывает имя экземпляра VMSS, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb741-130">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb741-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb741-131">-Confirm</span></span>
<span data-ttu-id="eb741-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eb741-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb741-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb741-133">-WhatIf</span></span>
<span data-ttu-id="eb741-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eb741-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb741-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eb741-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb741-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb741-136">CommonParameters</span></span>
<span data-ttu-id="eb741-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb741-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb741-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb741-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb741-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb741-139">INPUTS</span></span>

### <span data-ttu-id="eb741-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eb741-140">System.String</span></span>

## <span data-ttu-id="eb741-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb741-141">OUTPUTS</span></span>

### <span data-ttu-id="eb741-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eb741-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eb741-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb741-143">NOTES</span></span>

## <span data-ttu-id="eb741-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb741-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb741-145">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="eb741-145">Get-AzVmssVM</span></span>](./Get-AzVmssVM.md)
