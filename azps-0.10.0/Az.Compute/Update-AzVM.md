---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 8dd18c97a1636e4b6422d58fa7aca28d8798001b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910442"
---
# <span data-ttu-id="cb388-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-101">Update-AzVM</span></span>

## <span data-ttu-id="cb388-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb388-102">SYNOPSIS</span></span>
<span data-ttu-id="cb388-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="cb388-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="cb388-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb388-104">SYNTAX</span></span>

### <span data-ttu-id="cb388-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb388-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb388-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb388-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb388-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb388-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb388-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cb388-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb388-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb388-109">DESCRIPTION</span></span>
<span data-ttu-id="cb388-110">Командлет **Update-AzVM** обновляет состояние виртуальной машины Azure до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="cb388-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb388-111">EXAMPLES</span></span>

### <span data-ttu-id="cb388-112">Пример 1: обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="cb388-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="cb388-113">Эта команда обновляет виртуальную машину $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cb388-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="cb388-114">Эта команда обновляет ее с помощью объекта виртуальной машины, хранящегося в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="cb388-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="cb388-115">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="cb388-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="cb388-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb388-116">PARAMETERS</span></span>

### <span data-ttu-id="cb388-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb388-117">-AsJob</span></span>
<span data-ttu-id="cb388-118">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cb388-118">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cb388-119">-AssignIdentity</span></span>
<span data-ttu-id="cb388-120">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb388-121">-DefaultProfile</span></span>
<span data-ttu-id="cb388-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb388-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-123">-ID</span><span class="sxs-lookup"><span data-stu-id="cb388-123">-Id</span></span>
<span data-ttu-id="cb388-124">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="cb388-125">-IdentityId</span></span>
<span data-ttu-id="cb388-126">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cb388-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="cb388-127">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="cb388-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="cb388-128">-IdentityType</span></span>
<span data-ttu-id="cb388-129">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="cb388-130">В настоящее время единственным поддерживаемым типом является "SystemAssigned", который неявным образом создает удостоверение.</span><span class="sxs-lookup"><span data-stu-id="cb388-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="cb388-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="cb388-132">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cb388-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb388-133">-ResourceGroupName</span></span>
<span data-ttu-id="cb388-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="cb388-135">-Tag</span></span>
<span data-ttu-id="cb388-136">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="cb388-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="cb388-137">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="cb388-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="cb388-138">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="cb388-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-139">-VM</span><span class="sxs-lookup"><span data-stu-id="cb388-139">-VM</span></span>
<span data-ttu-id="cb388-140">Указывает локальный объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="cb388-141">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cb388-141">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="cb388-142">Этот объект виртуальной машины включает обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb388-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb388-143">-Confirm</span></span>
<span data-ttu-id="cb388-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb388-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb388-145">-WhatIf</span></span>
<span data-ttu-id="cb388-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb388-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cb388-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb388-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb388-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb388-148">CommonParameters</span></span>
<span data-ttu-id="cb388-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb388-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb388-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb388-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb388-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb388-151">INPUTS</span></span>

### <span data-ttu-id="cb388-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cb388-152">PSVirtualMachine</span></span>
<span data-ttu-id="cb388-153">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cb388-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="cb388-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb388-154">OUTPUTS</span></span>

### <span data-ttu-id="cb388-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cb388-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cb388-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb388-156">NOTES</span></span>

## <span data-ttu-id="cb388-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb388-157">RELATED LINKS</span></span>

[<span data-ttu-id="cb388-158">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-158">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="cb388-159">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-159">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="cb388-160">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-160">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="cb388-161">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-161">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="cb388-162">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-162">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="cb388-163">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="cb388-163">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="cb388-164">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="cb388-164">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


