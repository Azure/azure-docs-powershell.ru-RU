---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566531"
---
# <span data-ttu-id="5ec10-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="5ec10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ec10-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec10-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec10-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ec10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ec10-104">SYNTAX</span></span>

### <span data-ttu-id="5ec10-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ec10-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec10-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec10-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec10-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec10-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ec10-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5ec10-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ec10-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ec10-109">DESCRIPTION</span></span>
<span data-ttu-id="5ec10-110">Командлет **Update-AzureRmVM** обновляет состояние виртуальной машины Azure до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="5ec10-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ec10-111">EXAMPLES</span></span>

### <span data-ttu-id="5ec10-112">Пример 1: обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5ec10-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="5ec10-113">Эта команда обновляет виртуальную машину $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5ec10-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="5ec10-114">Эта команда обновляет ее с помощью объекта виртуальной машины, хранящегося в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5ec10-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5ec10-115">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="5ec10-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="5ec10-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ec10-116">PARAMETERS</span></span>

### <span data-ttu-id="5ec10-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ec10-117">-AsJob</span></span>
<span data-ttu-id="5ec10-118">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="5ec10-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5ec10-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5ec10-119">-AssignIdentity</span></span>
<span data-ttu-id="5ec10-120">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="5ec10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec10-121">-DefaultProfile</span></span>
<span data-ttu-id="5ec10-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec10-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ec10-123">-ID</span><span class="sxs-lookup"><span data-stu-id="5ec10-123">-Id</span></span>
<span data-ttu-id="5ec10-124">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="5ec10-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="5ec10-125">-IdentityId</span></span>
<span data-ttu-id="5ec10-126">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="5ec10-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="5ec10-127">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="5ec10-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="5ec10-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5ec10-128">-IdentityType</span></span>
<span data-ttu-id="5ec10-129">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="5ec10-130">В настоящее время единственным поддерживаемым типом является "SystemAssigned", который неявным образом создает удостоверение.</span><span class="sxs-lookup"><span data-stu-id="5ec10-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="5ec10-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="5ec10-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="5ec10-132">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5ec10-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="5ec10-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ec10-133">-ResourceGroupName</span></span>
<span data-ttu-id="5ec10-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5ec10-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="5ec10-135">-Tag</span></span>
<span data-ttu-id="5ec10-136">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="5ec10-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="5ec10-137">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="5ec10-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="5ec10-138">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="5ec10-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="5ec10-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="5ec10-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="5ec10-140">Флаг, позволяющий включать и отключать возможность использования одного или нескольких дисков управляемых данных с UltraSSD_LRS типом учетной записи хранения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5ec10-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="5ec10-141">Управляемые диски с типом учетной записи хранения UltraSSD_LRS можно добавлять на виртуальную машину только в том случае, если включено это свойство.</span><span class="sxs-lookup"><span data-stu-id="5ec10-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="5ec10-142">-VM</span><span class="sxs-lookup"><span data-stu-id="5ec10-142">-VM</span></span>
<span data-ttu-id="5ec10-143">Указывает локальный объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="5ec10-144">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5ec10-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="5ec10-145">Этот объект виртуальной машины включает обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5ec10-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="5ec10-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ec10-146">-Confirm</span></span>
<span data-ttu-id="5ec10-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ec10-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec10-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec10-148">-WhatIf</span></span>
<span data-ttu-id="5ec10-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ec10-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ec10-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ec10-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec10-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec10-151">CommonParameters</span></span>
<span data-ttu-id="5ec10-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ec10-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec10-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec10-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec10-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ec10-154">INPUTS</span></span>

### <span data-ttu-id="5ec10-155">System. String</span><span class="sxs-lookup"><span data-stu-id="5ec10-155">System.String</span></span>

### <span data-ttu-id="5ec10-156">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5ec10-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5ec10-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ec10-157">OUTPUTS</span></span>

### <span data-ttu-id="5ec10-158">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5ec10-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5ec10-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ec10-159">NOTES</span></span>

## <span data-ttu-id="5ec10-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ec10-160">RELATED LINKS</span></span>

[<span data-ttu-id="5ec10-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5ec10-162">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="5ec10-163">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5ec10-164">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5ec10-165">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5ec10-166">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ec10-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5ec10-167">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5ec10-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


