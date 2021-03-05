---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: a29e21bba3d04ca301d5f2bf3d2b5f9050fe9765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994479"
---
# <span data-ttu-id="f1ea3-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-101">Restart-AzVmss</span></span>

## <span data-ttu-id="f1ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ea3-103">Перезапуск VMSS или виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="f1ea3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1ea3-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ea3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ea3-106">Для **перезапуска на azvmss** перезапустится набор масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f1ea3-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f1ea3-107">Этот cmdlet также можно использовать для перезапуска определенной виртуальной машины внутри VMSS с помощью *параметра InstanceId.*</span><span class="sxs-lookup"><span data-stu-id="f1ea3-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="f1ea3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-108">EXAMPLES</span></span>

### <span data-ttu-id="f1ea3-109">Пример 1. Перезапуск VMSS</span><span class="sxs-lookup"><span data-stu-id="f1ea3-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="f1ea3-110">Эта команда перезапустит VMSS с именем VMSS001, которая принадлежит к группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="f1ea3-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="f1ea3-111">Пример 2. Перезапуск определенной виртуальной машины в VMSS</span><span class="sxs-lookup"><span data-stu-id="f1ea3-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f1ea3-112">Эта команда перезапустит виртуальную машину с ИД экземпляра 1 в VMSS под названием VMSS001, который принадлежит группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="f1ea3-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f1ea3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1ea3-113">PARAMETERS</span></span>

### <span data-ttu-id="f1ea3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1ea3-114">-AsJob</span></span>
<span data-ttu-id="f1ea3-115">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f1ea3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ea3-116">-DefaultProfile</span></span>
<span data-ttu-id="f1ea3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1ea3-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f1ea3-118">-InstanceId</span></span>
<span data-ttu-id="f1ea3-119">Указывает, что в качестве строки массива указывается ИД экземпляров, которые необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ea3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ea3-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1ea3-121">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f1ea3-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f1ea3-122">-VMScaleSetName</span></span>
<span data-ttu-id="f1ea3-123">Вид имени VMSS, который перезапустится этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="f1ea3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1ea3-124">-Confirm</span></span>
<span data-ttu-id="f1ea3-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ea3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ea3-126">-WhatIf</span></span>
<span data-ttu-id="f1ea3-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1ea3-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ea3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ea3-129">CommonParameters</span></span>
<span data-ttu-id="f1ea3-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ea3-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1ea3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ea3-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1ea3-132">INPUTS</span></span>

### <span data-ttu-id="f1ea3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f1ea3-133">System.String</span></span>

### <span data-ttu-id="f1ea3-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f1ea3-134">System.String[]</span></span>

## <span data-ttu-id="f1ea3-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1ea3-135">OUTPUTS</span></span>

### <span data-ttu-id="f1ea3-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f1ea3-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f1ea3-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-137">NOTES</span></span>

## <span data-ttu-id="f1ea3-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1ea3-138">RELATED LINKS</span></span>

[<span data-ttu-id="f1ea3-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f1ea3-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="f1ea3-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f1ea3-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="f1ea3-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f1ea3-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="f1ea3-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f1ea3-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


