---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
ms.openlocfilehash: 55f7b56f57bf18c4a3bf3198e8335cff08caae97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557475"
---
# <span data-ttu-id="4a5eb-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="4a5eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5eb-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a5eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a5eb-104">SYNTAX</span></span>

### <span data-ttu-id="4a5eb-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a5eb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a5eb-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a5eb-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a5eb-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a5eb-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a5eb-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4a5eb-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a5eb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a5eb-109">DESCRIPTION</span></span>
<span data-ttu-id="4a5eb-110">Командлет **Update-AzureRmVM** обновляет состояние виртуальной машины Azure до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="4a5eb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a5eb-111">EXAMPLES</span></span>

### <span data-ttu-id="4a5eb-112">Пример 1: обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4a5eb-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4a5eb-113">Эта команда обновляет виртуальную машину $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="4a5eb-114">Эта команда обновляет ее с помощью объекта виртуальной машины, хранящегося в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4a5eb-115">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="4a5eb-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="4a5eb-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a5eb-116">PARAMETERS</span></span>

### <span data-ttu-id="4a5eb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a5eb-117">-AsJob</span></span>
<span data-ttu-id="4a5eb-118">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4a5eb-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4a5eb-119">-AssignIdentity</span></span>
<span data-ttu-id="4a5eb-120">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="4a5eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5eb-121">-DefaultProfile</span></span>
<span data-ttu-id="4a5eb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a5eb-123">-ID</span><span class="sxs-lookup"><span data-stu-id="4a5eb-123">-Id</span></span>
<span data-ttu-id="4a5eb-124">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="4a5eb-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="4a5eb-125">-IdentityId</span></span>
<span data-ttu-id="4a5eb-126">Указывает список удостоверений пользователей, связанных с набором масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="4a5eb-127">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="4a5eb-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="4a5eb-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4a5eb-128">-IdentityType</span></span>
<span data-ttu-id="4a5eb-129">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="4a5eb-130">В настоящее время единственным поддерживаемым типом является "SystemAssigned", который неявным образом создает удостоверение.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="4a5eb-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4a5eb-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="4a5eb-132">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="4a5eb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5eb-133">-ResourceGroupName</span></span>
<span data-ttu-id="4a5eb-134">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4a5eb-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="4a5eb-135">-Tag</span></span>
<span data-ttu-id="4a5eb-136">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="4a5eb-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="4a5eb-137">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="4a5eb-138">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="4a5eb-139">-VM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-139">-VM</span></span>
<span data-ttu-id="4a5eb-140">Указывает локальный объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="4a5eb-141">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-141">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="4a5eb-142">Этот объект виртуальной машины включает обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="4a5eb-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a5eb-143">-Confirm</span></span>
<span data-ttu-id="4a5eb-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5eb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5eb-145">-WhatIf</span></span>
<span data-ttu-id="4a5eb-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4a5eb-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a5eb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5eb-148">CommonParameters</span></span>
<span data-ttu-id="4a5eb-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5eb-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a5eb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5eb-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a5eb-151">INPUTS</span></span>

### <span data-ttu-id="4a5eb-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4a5eb-152">PSVirtualMachine</span></span>
<span data-ttu-id="4a5eb-153">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4a5eb-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="4a5eb-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a5eb-154">OUTPUTS</span></span>

### <span data-ttu-id="4a5eb-155">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4a5eb-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4a5eb-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a5eb-156">NOTES</span></span>

## <span data-ttu-id="4a5eb-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a5eb-157">RELATED LINKS</span></span>

[<span data-ttu-id="4a5eb-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4a5eb-159">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-159">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="4a5eb-160">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-160">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="4a5eb-161">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-161">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="4a5eb-162">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-162">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="4a5eb-163">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4a5eb-163">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="4a5eb-164">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4a5eb-164">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


