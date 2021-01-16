---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: c686eec33a2f4a9f972acbdb7261f86fc45a6fa1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412223"
---
# <span data-ttu-id="cab0a-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-101">Restart-AzVmss</span></span>

## <span data-ttu-id="cab0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab0a-102">SYNOPSIS</span></span>
<span data-ttu-id="cab0a-103">Перезапуск VMSS или виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="cab0a-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="cab0a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cab0a-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab0a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cab0a-105">DESCRIPTION</span></span>
<span data-ttu-id="cab0a-106">Для **перезапуска на azvmss** перезапустится набор масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cab0a-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="cab0a-107">Этот cmdlet также можно использовать для перезапуска определенной виртуальной машины внутри VMSS с помощью *параметра InstanceId.*</span><span class="sxs-lookup"><span data-stu-id="cab0a-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="cab0a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cab0a-108">EXAMPLES</span></span>

### <span data-ttu-id="cab0a-109">Пример 1. Перезапуск VMSS</span><span class="sxs-lookup"><span data-stu-id="cab0a-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="cab0a-110">Эта команда перезапустит VMSS с именем VMSS001, которая принадлежит к группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="cab0a-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="cab0a-111">Пример 2. Перезапуск определенной виртуальной машины в VMSS</span><span class="sxs-lookup"><span data-stu-id="cab0a-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="cab0a-112">Эта команда перезапустит виртуальную машину с ИД экземпляра 1 в VMSS под названием VMSS001, который принадлежит группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="cab0a-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="cab0a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cab0a-113">PARAMETERS</span></span>

### <span data-ttu-id="cab0a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cab0a-114">-AsJob</span></span>
<span data-ttu-id="cab0a-115">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cab0a-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cab0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab0a-116">-DefaultProfile</span></span>
<span data-ttu-id="cab0a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cab0a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab0a-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cab0a-118">-InstanceId</span></span>
<span data-ttu-id="cab0a-119">Указывает, что в качестве строки массива указаны ИД экземпляров, которые необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="cab0a-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="cab0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="cab0a-121">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="cab0a-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="cab0a-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cab0a-122">-VMScaleSetName</span></span>
<span data-ttu-id="cab0a-123">Вид имени VMSS, который будет перезапускать этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab0a-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="cab0a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cab0a-124">-Confirm</span></span>
<span data-ttu-id="cab0a-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cab0a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab0a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab0a-126">-WhatIf</span></span>
<span data-ttu-id="cab0a-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab0a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cab0a-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cab0a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab0a-129">CommonParameters</span></span>
<span data-ttu-id="cab0a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab0a-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cab0a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab0a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cab0a-132">INPUTS</span></span>

### <span data-ttu-id="cab0a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cab0a-133">System.String</span></span>

### <span data-ttu-id="cab0a-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cab0a-134">System.String[]</span></span>

## <span data-ttu-id="cab0a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cab0a-135">OUTPUTS</span></span>

### <span data-ttu-id="cab0a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cab0a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cab0a-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cab0a-137">NOTES</span></span>

## <span data-ttu-id="cab0a-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cab0a-138">RELATED LINKS</span></span>

[<span data-ttu-id="cab0a-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="cab0a-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="cab0a-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="cab0a-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="cab0a-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="cab0a-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="cab0a-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cab0a-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


