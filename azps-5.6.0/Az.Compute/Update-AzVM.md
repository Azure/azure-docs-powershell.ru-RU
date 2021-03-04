---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e7a86b191687f72cb538fb017a904890e4958d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955971"
---
# <span data-ttu-id="65e67-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="65e67-101">Update-AzVM</span></span>

## <span data-ttu-id="65e67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e67-102">SYNOPSIS</span></span>
<span data-ttu-id="65e67-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="65e67-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="65e67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65e67-104">SYNTAX</span></span>

### <span data-ttu-id="65e67-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65e67-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e67-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="65e67-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65e67-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="65e67-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65e67-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65e67-108">DESCRIPTION</span></span>
<span data-ttu-id="65e67-109">С **использованием cmdlet Update-AzVM** состояние виртуальной машины Azure обновляется до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="65e67-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65e67-110">EXAMPLES</span></span>

### <span data-ttu-id="65e67-111">Пример 1. Обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="65e67-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="65e67-112">Эта команда обновляет виртуальную машину ($VirtualMachine) в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="65e67-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="65e67-113">Команда обновляет ее с помощью объекта виртуальной машины, который хранится в переменной $VirtualMachine компьютера.</span><span class="sxs-lookup"><span data-stu-id="65e67-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="65e67-114">Чтобы получить объект виртуальной машины, используйте **cmdlet Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="65e67-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="65e67-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65e67-115">PARAMETERS</span></span>

### <span data-ttu-id="65e67-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65e67-116">-AsJob</span></span>
<span data-ttu-id="65e67-117">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="65e67-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="65e67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e67-118">-DefaultProfile</span></span>
<span data-ttu-id="65e67-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65e67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65e67-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="65e67-120">-HostId</span></span>
<span data-ttu-id="65e67-121">ИД хоста</span><span class="sxs-lookup"><span data-stu-id="65e67-121">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e67-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="65e67-122">-EncryptionAtHost</span></span>
<span data-ttu-id="65e67-123">Свойство EncryptionAtHost может использоваться пользователем в запросе для того, чтобы включить или отключить шифрование хоста для набора масштаба виртуальной машины или виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="65e67-124">Это позволит шифровать все диски, включая диск Resource/Temp на самом хосте.</span><span class="sxs-lookup"><span data-stu-id="65e67-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e67-125">-Id</span><span class="sxs-lookup"><span data-stu-id="65e67-125">-Id</span></span>
<span data-ttu-id="65e67-126">Определяет ИД ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-126">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="65e67-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="65e67-127">-IdentityId</span></span>
<span data-ttu-id="65e67-128">Определяет список удостоверений пользователей, связанных с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="65e67-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="65e67-129">Ссылки на удостоверения пользователей будут ARM в форме: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="65e67-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="65e67-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="65e67-130">-IdentityType</span></span>
<span data-ttu-id="65e67-131">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="65e67-132">Допустимые значения: SystemAssigned, UserAssigned, SystemAssignedUserAssigned и None.</span><span class="sxs-lookup"><span data-stu-id="65e67-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="65e67-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="65e67-133">-MaxPrice</span></span>
<span data-ttu-id="65e67-134">Указывает максимальную цену, которую вы будете оплачивать для службы VM или VMSS с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="65e67-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="65e67-135">Эта цена в долларах США.</span><span class="sxs-lookup"><span data-stu-id="65e67-135">This price is in US Dollars.</span></span> <span data-ttu-id="65e67-136">Эта цена будет сравниваться с текущей низкой ценой приоритета для размера VM.</span><span class="sxs-lookup"><span data-stu-id="65e67-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="65e67-137">Кроме того, цены сравниваются во время создания или обновления низкой приоритетной VM-или VMSS и операция будет работать только в том случае, если максимальная цена больше текущей цены с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="65e67-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="65e67-138">Максимальное значение maxPrice также будет использоваться для создания обетовки VM или VMSS с низким приоритетом, если текущая цена с низким приоритетом выходит за пределы максимальной цены после создания VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="65e67-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="65e67-139">Возможные значения: любое десятичее значение больше нуля.</span><span class="sxs-lookup"><span data-stu-id="65e67-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="65e67-140">Пример: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="65e67-140">Example: 0.01538.</span></span>  <span data-ttu-id="65e67-141">-1 указывает на то, что не следует переумелять VM или VMSS с низким приоритетом по ценам.</span><span class="sxs-lookup"><span data-stu-id="65e67-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="65e67-142">Кроме того, максимальная цена по умолчанию составляет -1, если она не предоставлена вами.</span><span class="sxs-lookup"><span data-stu-id="65e67-142">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="65e67-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="65e67-143">-NoWait</span></span>
<span data-ttu-id="65e67-144">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="65e67-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="65e67-145">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="65e67-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="65e67-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="65e67-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="65e67-147">Указывает, следует ли включить или отключить WriteAccelerator на диске ОС.</span><span class="sxs-lookup"><span data-stu-id="65e67-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="65e67-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="65e67-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="65e67-149">ИД ресурса группы расположения близости, который можно использовать с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="65e67-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e67-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e67-150">-ResourceGroupName</span></span>
<span data-ttu-id="65e67-151">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e67-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="65e67-152">-Tag</span></span>
<span data-ttu-id="65e67-153">Определяет, что ресурсы и группы ресурсов могут быть помечены парой имен и значений.</span><span class="sxs-lookup"><span data-stu-id="65e67-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="65e67-154">Добавив теги к ресурсам, вы сможете сгруппить ресурсы в группах ресурсов и создать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="65e67-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="65e67-155">Каждая группа ресурсов может иметь не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="65e67-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="65e67-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="65e67-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="65e67-157">Флаг, который позволяет или отключает возможность иметь один или несколько управляемых дисков данных с типом учетной UltraSSD_LRS хранения на VM.</span><span class="sxs-lookup"><span data-stu-id="65e67-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="65e67-158">Управляемые диски с типом учетной UltraSSD_LRS можно добавить на виртуальную машину, только если это свойство включено.</span><span class="sxs-lookup"><span data-stu-id="65e67-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="65e67-159">-VM</span><span class="sxs-lookup"><span data-stu-id="65e67-159">-VM</span></span>
<span data-ttu-id="65e67-160">Указывает объект локальной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="65e67-161">Чтобы получить объект виртуальной машины, воспользуйтесь Get-AzVM..</span><span class="sxs-lookup"><span data-stu-id="65e67-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="65e67-162">Этот объект виртуальной машины содержит обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65e67-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="65e67-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65e67-163">-Confirm</span></span>
<span data-ttu-id="65e67-164">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e67-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65e67-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65e67-165">-WhatIf</span></span>
<span data-ttu-id="65e67-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e67-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65e67-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="65e67-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="65e67-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e67-168">CommonParameters</span></span>
<span data-ttu-id="65e67-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e67-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e67-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65e67-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e67-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65e67-171">INPUTS</span></span>

### <span data-ttu-id="65e67-172">System.String</span><span class="sxs-lookup"><span data-stu-id="65e67-172">System.String</span></span>

### <span data-ttu-id="65e67-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="65e67-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="65e67-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65e67-174">System.Boolean</span></span>

## <span data-ttu-id="65e67-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65e67-175">OUTPUTS</span></span>

### <span data-ttu-id="65e67-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="65e67-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="65e67-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65e67-177">NOTES</span></span>

## <span data-ttu-id="65e67-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65e67-178">RELATED LINKS</span></span>

[<span data-ttu-id="65e67-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="65e67-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="65e67-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="65e67-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="65e67-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="65e67-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="65e67-182">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="65e67-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="65e67-183">Start-AzvM</span><span class="sxs-lookup"><span data-stu-id="65e67-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="65e67-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="65e67-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="65e67-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="65e67-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


