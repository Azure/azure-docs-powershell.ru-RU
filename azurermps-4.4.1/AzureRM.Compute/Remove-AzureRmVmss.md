---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 703fc0d83fb17e1131c44cbd06593887ebcce020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557871"
---
# <span data-ttu-id="f4757-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="f4757-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4757-102">SYNOPSIS</span></span>
<span data-ttu-id="f4757-103">Удаление VMSS или виртуальной машины, которая находится в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4757-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4757-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4757-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4757-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4757-105">DESCRIPTION</span></span>
<span data-ttu-id="f4757-106">Командлет **Remove-AzureRmVmss** удаляет из Azure (VMSS) установленный параметр "виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="f4757-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="f4757-107">Этот командлет также можно использовать для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4757-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="f4757-108">Вы можете использовать параметр *InstanceId* для удаления определенной виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4757-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="f4757-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4757-109">EXAMPLES</span></span>

### <span data-ttu-id="f4757-110">Пример 1: удаление VMSS</span><span class="sxs-lookup"><span data-stu-id="f4757-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="f4757-111">Эта команда удаляет VMSS с именем VMScaleSet001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="f4757-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="f4757-112">Пример 2: Удаление виртуальной машины из VMSS</span><span class="sxs-lookup"><span data-stu-id="f4757-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="f4757-113">Эта команда удаляет виртуальную машину с ИДЕНТИФИКАТОРом 3 из VMSS с именем VMScaleSet002, которая относится к группе ресурсов с именем Group002.</span><span class="sxs-lookup"><span data-stu-id="f4757-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="f4757-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4757-114">PARAMETERS</span></span>

### <span data-ttu-id="f4757-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4757-115">-DefaultProfile</span></span>
<span data-ttu-id="f4757-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4757-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4757-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f4757-117">-Force</span></span>
<span data-ttu-id="f4757-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4757-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4757-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f4757-119">-InstanceId</span></span>
<span data-ttu-id="f4757-120">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо запустить.</span><span class="sxs-lookup"><span data-stu-id="f4757-120">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="f4757-121">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="f4757-121">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="f4757-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4757-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4757-123">Указывает имя группы ресурсов, к которой относится VMSS.</span><span class="sxs-lookup"><span data-stu-id="f4757-123">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="f4757-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f4757-124">-VMScaleSetName</span></span>
<span data-ttu-id="f4757-125">Форель имя VMSS, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4757-125">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="f4757-126">Если вы укажете параметр *InstanceId* , командлет удалит указанную виртуальную машину из VMSS с именем, указанным в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="f4757-126">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="f4757-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4757-127">-Confirm</span></span>
<span data-ttu-id="f4757-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4757-128">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="f4757-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4757-129">-WhatIf</span></span>
<span data-ttu-id="f4757-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4757-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4757-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4757-131">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="f4757-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4757-132">CommonParameters</span></span>
<span data-ttu-id="f4757-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4757-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4757-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4757-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4757-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4757-135">INPUTS</span></span>

## <span data-ttu-id="f4757-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4757-136">OUTPUTS</span></span>

## <span data-ttu-id="f4757-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4757-137">NOTES</span></span>

## <span data-ttu-id="f4757-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4757-138">RELATED LINKS</span></span>

[<span data-ttu-id="f4757-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="f4757-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f4757-141">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="f4757-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="f4757-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f4757-144">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="f4757-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f4757-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


