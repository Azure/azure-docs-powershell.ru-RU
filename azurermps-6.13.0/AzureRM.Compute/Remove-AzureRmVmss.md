---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 54c6f9f399cfabf7a418939b4662c9bcfdc83d34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567800"
---
# <span data-ttu-id="10806-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="10806-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10806-102">SYNOPSIS</span></span>
<span data-ttu-id="10806-103">Удаление VMSS или виртуальной машины, которая находится в VMSS.</span><span class="sxs-lookup"><span data-stu-id="10806-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10806-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10806-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10806-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10806-105">DESCRIPTION</span></span>
<span data-ttu-id="10806-106">Командлет **Remove-AzureRmVmss** удаляет из Azure (VMSS) установленный параметр "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="10806-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="10806-107">Этот командлет также можно использовать для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="10806-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="10806-108">Вы можете использовать параметр *InstanceId* для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="10806-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="10806-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10806-109">EXAMPLES</span></span>

### <span data-ttu-id="10806-110">Пример 1: удаление VMSS</span><span class="sxs-lookup"><span data-stu-id="10806-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="10806-111">Эта команда удаляет VMSS с именем VMScaleSet001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="10806-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="10806-112">Пример 2: Удаление виртуальной машины из VMSS</span><span class="sxs-lookup"><span data-stu-id="10806-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="10806-113">Эта команда удаляет виртуальную машину с ИДЕНТИФИКАТОРом 3 из VMSS с именем VMScaleSet002, которая относится к группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="10806-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="10806-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10806-114">PARAMETERS</span></span>

### <span data-ttu-id="10806-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10806-115">-AsJob</span></span>
<span data-ttu-id="10806-116">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="10806-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="10806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10806-117">-DefaultProfile</span></span>
<span data-ttu-id="10806-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10806-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10806-119">-Force</span><span class="sxs-lookup"><span data-stu-id="10806-119">-Force</span></span>
<span data-ttu-id="10806-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="10806-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10806-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="10806-121">-InstanceId</span></span>
<span data-ttu-id="10806-122">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="10806-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="10806-123">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="10806-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10806-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10806-124">-ResourceGroupName</span></span>
<span data-ttu-id="10806-125">Указывает имя группы ресурсов, к которой относится VMSS.</span><span class="sxs-lookup"><span data-stu-id="10806-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="10806-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="10806-126">-VMScaleSetName</span></span>
<span data-ttu-id="10806-127">Форель имя VMSS, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10806-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="10806-128">Если вы укажете параметр *InstanceId* , командлет удалит указанную виртуальную машину из VMSS с именем, указанным в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="10806-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10806-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10806-129">-Confirm</span></span>
<span data-ttu-id="10806-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="10806-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10806-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10806-131">-WhatIf</span></span>
<span data-ttu-id="10806-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="10806-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10806-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="10806-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10806-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10806-134">CommonParameters</span></span>
<span data-ttu-id="10806-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10806-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10806-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10806-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10806-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10806-137">INPUTS</span></span>

### <span data-ttu-id="10806-138">System. String</span><span class="sxs-lookup"><span data-stu-id="10806-138">System.String</span></span>

### <span data-ttu-id="10806-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="10806-139">System.String[]</span></span>

## <span data-ttu-id="10806-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10806-140">OUTPUTS</span></span>

### <span data-ttu-id="10806-141">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="10806-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="10806-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="10806-142">NOTES</span></span>

## <span data-ttu-id="10806-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10806-143">RELATED LINKS</span></span>

[<span data-ttu-id="10806-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="10806-145">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="10806-146">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="10806-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="10806-148">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="10806-149">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="10806-150">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="10806-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


