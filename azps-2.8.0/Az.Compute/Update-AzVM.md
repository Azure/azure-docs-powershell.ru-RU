---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 339d63fe02c8286dc5867428269dc2e2afe342d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721623"
---
# <span data-ttu-id="b3fab-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-101">Update-AzVM</span></span>

## <span data-ttu-id="b3fab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3fab-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fab-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="b3fab-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="b3fab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3fab-104">SYNTAX</span></span>

### <span data-ttu-id="b3fab-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3fab-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3fab-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3fab-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3fab-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3fab-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3fab-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b3fab-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3fab-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3fab-109">DESCRIPTION</span></span>
<span data-ttu-id="b3fab-110">Командлет **Update-AzVM** обновляет состояние виртуальной машины Azure до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="b3fab-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3fab-111">EXAMPLES</span></span>

### <span data-ttu-id="b3fab-112">Пример 1: обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="b3fab-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b3fab-113">Эта команда обновляет виртуальную машину $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b3fab-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="b3fab-114">Эта команда обновляет ее с помощью объекта виртуальной машины, хранящегося в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b3fab-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b3fab-115">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="b3fab-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="b3fab-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3fab-116">PARAMETERS</span></span>

### <span data-ttu-id="b3fab-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3fab-117">-AsJob</span></span>
<span data-ttu-id="b3fab-118">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="b3fab-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3fab-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b3fab-119">-AssignIdentity</span></span>
<span data-ttu-id="b3fab-120">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fab-121">-DefaultProfile</span></span>
<span data-ttu-id="b3fab-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3fab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3fab-123">-ID</span><span class="sxs-lookup"><span data-stu-id="b3fab-123">-Id</span></span>
<span data-ttu-id="b3fab-124">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-124">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="b3fab-125">-IdentityId</span></span>
<span data-ttu-id="b3fab-126">Указывает список удостоверений пользователей, связанных с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="b3fab-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="b3fab-127">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="b3fab-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b3fab-128">-IdentityType</span></span>
<span data-ttu-id="b3fab-129">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="b3fab-130">Допустимые значения: "SystemAssigned", "UserAssigned", "SystemAssignedUserAssigned" и "нет".</span><span class="sxs-lookup"><span data-stu-id="b3fab-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="b3fab-131">-MaxPrice</span></span>
<span data-ttu-id="b3fab-132">Максимальная цена, которую вы хотите заплатить за низкий приоритет ВМ или VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3fab-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="b3fab-133">Эта стоимость указана в долларах США.</span><span class="sxs-lookup"><span data-stu-id="b3fab-133">This price is in US Dollars.</span></span> <span data-ttu-id="b3fab-134">Эта цена будет сравниваться с ценой с низким приоритетом для размера ВМ.</span><span class="sxs-lookup"><span data-stu-id="b3fab-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="b3fab-135">Кроме того, цены проверяются во время создания или обновления виртуальной машины или VMSS, а операция будет выполнена только в том случае, если значение maxPrice больше, чем текущая цена с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="b3fab-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="b3fab-136">MaxPrice также будет использоваться для удаления слабого приоритета ВМ/VMSS, если текущая цена с низким приоритетом выходит за пределы maxPrice после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="b3fab-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="b3fab-137">Возможные значения: Любое десятичное значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="b3fab-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="b3fab-138">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="b3fab-138">Example: 0.01538.</span></span>  <span data-ttu-id="b3fab-139">-1 указывает на то, что низкий приоритет VM/VMSS не следует выключать для целей цены.</span><span class="sxs-lookup"><span data-stu-id="b3fab-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="b3fab-140">Кроме того, максимальная цена по умолчанию составляет-1, если она не предоставляется вам.</span><span class="sxs-lookup"><span data-stu-id="b3fab-140">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-141">-Wait</span><span class="sxs-lookup"><span data-stu-id="b3fab-141">-NoWait</span></span>
<span data-ttu-id="b3fab-142">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="b3fab-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="b3fab-143">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="b3fab-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="b3fab-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b3fab-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="b3fab-145">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="b3fab-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3fab-146">-ResourceGroupName</span></span>
<span data-ttu-id="b3fab-147">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-147">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="b3fab-148">-Tag</span></span>
<span data-ttu-id="b3fab-149">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="b3fab-149">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="b3fab-150">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="b3fab-150">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="b3fab-151">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="b3fab-151">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="b3fab-152">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="b3fab-152">-UltraSSDEnabled</span></span>
<span data-ttu-id="b3fab-153">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с UltraSSD_LRS типом учетной записи хранения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b3fab-153">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="b3fab-154">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять на виртуальную машину только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="b3fab-154">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-155">-VM</span><span class="sxs-lookup"><span data-stu-id="b3fab-155">-VM</span></span>
<span data-ttu-id="b3fab-156">Указывает локальный объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-156">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="b3fab-157">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b3fab-157">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="b3fab-158">Этот объект виртуальной машины включает обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b3fab-158">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3fab-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3fab-159">-Confirm</span></span>
<span data-ttu-id="b3fab-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3fab-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3fab-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3fab-161">-WhatIf</span></span>
<span data-ttu-id="b3fab-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3fab-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3fab-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3fab-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3fab-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fab-164">CommonParameters</span></span>
<span data-ttu-id="b3fab-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3fab-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fab-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3fab-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fab-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3fab-167">INPUTS</span></span>

### <span data-ttu-id="b3fab-168">System. String</span><span class="sxs-lookup"><span data-stu-id="b3fab-168">System.String</span></span>

### <span data-ttu-id="b3fab-169">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b3fab-169">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b3fab-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3fab-170">System.Boolean</span></span>

## <span data-ttu-id="b3fab-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3fab-171">OUTPUTS</span></span>

### <span data-ttu-id="b3fab-172">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b3fab-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b3fab-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3fab-173">NOTES</span></span>

## <span data-ttu-id="b3fab-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3fab-174">RELATED LINKS</span></span>

[<span data-ttu-id="b3fab-175">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-175">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b3fab-176">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-176">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="b3fab-177">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-177">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="b3fab-178">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-178">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="b3fab-179">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-179">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="b3fab-180">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="b3fab-180">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="b3fab-181">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b3fab-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


