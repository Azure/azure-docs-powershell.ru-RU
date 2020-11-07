---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901061"
---
# <span data-ttu-id="f7990-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-101">Update-AzVM</span></span>

## <span data-ttu-id="f7990-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7990-102">SYNOPSIS</span></span>
<span data-ttu-id="f7990-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="f7990-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="f7990-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7990-104">SYNTAX</span></span>

### <span data-ttu-id="f7990-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7990-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7990-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7990-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7990-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7990-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7990-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f7990-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7990-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7990-109">DESCRIPTION</span></span>
<span data-ttu-id="f7990-110">Командлет **Update-AzVM** обновляет состояние виртуальной машины Azure до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="f7990-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7990-111">EXAMPLES</span></span>

### <span data-ttu-id="f7990-112">Пример 1: обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f7990-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="f7990-113">Эта команда обновляет виртуальную машину $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f7990-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="f7990-114">Эта команда обновляет ее с помощью объекта виртуальной машины, хранящегося в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="f7990-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="f7990-115">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="f7990-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="f7990-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7990-116">PARAMETERS</span></span>

### <span data-ttu-id="f7990-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7990-117">-AsJob</span></span>
<span data-ttu-id="f7990-118">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f7990-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f7990-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f7990-119">-AssignIdentity</span></span>
<span data-ttu-id="f7990-120">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="f7990-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7990-121">-DefaultProfile</span></span>
<span data-ttu-id="f7990-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7990-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7990-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f7990-123">-Id</span></span>
<span data-ttu-id="f7990-124">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="f7990-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="f7990-125">-IdentityId</span></span>
<span data-ttu-id="f7990-126">Указывает список удостоверений пользователей, связанных с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="f7990-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="f7990-127">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="f7990-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="f7990-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f7990-128">-IdentityType</span></span>
<span data-ttu-id="f7990-129">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="f7990-130">Допустимые значения: "SystemAssigned", "UserAssigned", "SystemAssignedUserAssigned" и "нет".</span><span class="sxs-lookup"><span data-stu-id="f7990-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="f7990-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="f7990-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="f7990-132">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f7990-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="f7990-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7990-133">-ResourceGroupName</span></span>
<span data-ttu-id="f7990-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f7990-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="f7990-135">-Tag</span></span>
<span data-ttu-id="f7990-136">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="f7990-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="f7990-137">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="f7990-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="f7990-138">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="f7990-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="f7990-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="f7990-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="f7990-140">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с UltraSSD_LRS типом учетной записи хранения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f7990-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="f7990-141">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять на виртуальную машину только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="f7990-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="f7990-142">-VM</span><span class="sxs-lookup"><span data-stu-id="f7990-142">-VM</span></span>
<span data-ttu-id="f7990-143">Указывает локальный объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="f7990-144">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f7990-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="f7990-145">Этот объект виртуальной машины включает обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f7990-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="f7990-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7990-146">-Confirm</span></span>
<span data-ttu-id="f7990-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7990-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7990-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7990-148">-WhatIf</span></span>
<span data-ttu-id="f7990-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7990-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7990-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7990-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7990-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7990-151">CommonParameters</span></span>
<span data-ttu-id="f7990-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7990-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7990-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7990-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7990-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7990-154">INPUTS</span></span>

### <span data-ttu-id="f7990-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f7990-155">System.String</span></span>

### <span data-ttu-id="f7990-156">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f7990-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f7990-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7990-157">System.Boolean</span></span>

## <span data-ttu-id="f7990-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7990-158">OUTPUTS</span></span>

### <span data-ttu-id="f7990-159">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f7990-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f7990-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7990-160">NOTES</span></span>

## <span data-ttu-id="f7990-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7990-161">RELATED LINKS</span></span>

[<span data-ttu-id="f7990-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f7990-163">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="f7990-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f7990-165">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="f7990-166">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f7990-167">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="f7990-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f7990-168">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f7990-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


