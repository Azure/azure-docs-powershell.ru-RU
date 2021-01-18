---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519420"
---
# <span data-ttu-id="e1265-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="e1265-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="e1265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1265-102">SYNOPSIS</span></span>
<span data-ttu-id="e1265-103">Запускает обновление экземпляра VMSS вручную.</span><span class="sxs-lookup"><span data-stu-id="e1265-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="e1265-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1265-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1265-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1265-105">DESCRIPTION</span></span>
<span data-ttu-id="e1265-106">С Update-AzVmssInstance запускается ручное обновление указанного экземпляра набора масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e1265-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="e1265-107">Это используется, когда политика обновления для набора масштаба VMSS настроена на ручную.</span><span class="sxs-lookup"><span data-stu-id="e1265-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="e1265-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1265-108">EXAMPLES</span></span>

### <span data-ttu-id="e1265-109">Пример 1. Запуск обновления экземпляра VMSS</span><span class="sxs-lookup"><span data-stu-id="e1265-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="e1265-110">Эта команда запускает обновление VMSS VMScaleSet001 с ИД экземпляра 0.</span><span class="sxs-lookup"><span data-stu-id="e1265-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="e1265-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1265-111">PARAMETERS</span></span>

### <span data-ttu-id="e1265-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1265-112">-AsJob</span></span>
<span data-ttu-id="e1265-113">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="e1265-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e1265-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1265-114">-DefaultProfile</span></span>
<span data-ttu-id="e1265-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1265-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1265-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e1265-116">-InstanceId</span></span>
<span data-ttu-id="e1265-117">Указывает, что это строка, а также ИД обновляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e1265-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1265-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1265-118">-ResourceGroupName</span></span>
<span data-ttu-id="e1265-119">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="e1265-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="e1265-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e1265-120">-VMScaleSetName</span></span>
<span data-ttu-id="e1265-121">Указывает имя экземпляра VMSS, который обновляется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1265-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="e1265-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1265-122">-Confirm</span></span>
<span data-ttu-id="e1265-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e1265-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1265-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1265-124">-WhatIf</span></span>
<span data-ttu-id="e1265-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1265-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1265-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e1265-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1265-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1265-127">CommonParameters</span></span>
<span data-ttu-id="e1265-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1265-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1265-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1265-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1265-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1265-130">INPUTS</span></span>

### <span data-ttu-id="e1265-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e1265-131">System.String</span></span>

### <span data-ttu-id="e1265-132">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e1265-132">System.String[]</span></span>

## <span data-ttu-id="e1265-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1265-133">OUTPUTS</span></span>

### <span data-ttu-id="e1265-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e1265-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e1265-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1265-135">NOTES</span></span>

## <span data-ttu-id="e1265-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1265-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1265-137">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e1265-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


