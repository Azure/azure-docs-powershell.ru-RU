---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566292"
---
# <span data-ttu-id="17d29-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="17d29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17d29-102">SYNOPSIS</span></span>
<span data-ttu-id="17d29-103">Обновляет состояние виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="17d29-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17d29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17d29-104">SYNTAX</span></span>

### <span data-ttu-id="17d29-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17d29-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17d29-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="17d29-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17d29-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17d29-107">DESCRIPTION</span></span>
<span data-ttu-id="17d29-108">Командлет **Update-AzureRmVM** обновляет состояние виртуальной машины Azure до состояния объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="17d29-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17d29-109">EXAMPLES</span></span>

### <span data-ttu-id="17d29-110">Пример 1: обновление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="17d29-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="17d29-111">Эта команда обновляет виртуальную машину $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="17d29-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="17d29-112">Эта команда обновляет ее с помощью объекта виртуальной машины, хранящегося в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="17d29-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="17d29-113">Чтобы получить объект виртуальной машины, используйте командлет **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="17d29-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="17d29-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17d29-114">PARAMETERS</span></span>

### <span data-ttu-id="17d29-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="17d29-115">-AssignIdentity</span></span>
<span data-ttu-id="17d29-116">Укажите учетную запись, назначенную системой для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="17d29-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d29-117">-DefaultProfile</span></span>
<span data-ttu-id="17d29-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17d29-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17d29-119">-ID</span><span class="sxs-lookup"><span data-stu-id="17d29-119">-Id</span></span>
<span data-ttu-id="17d29-120">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="17d29-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="17d29-121">-IdentityType</span></span>
<span data-ttu-id="17d29-122">Тип удостоверения, используемого для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="17d29-123">В настоящее время единственным поддерживаемым типом является "SystemAssigned", который неявным образом создает удостоверение.</span><span class="sxs-lookup"><span data-stu-id="17d29-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d29-124">-ResourceGroupName</span></span>
<span data-ttu-id="17d29-125">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17d29-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="17d29-126">-Tags</span></span>
<span data-ttu-id="17d29-127">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="17d29-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="17d29-128">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="17d29-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="17d29-129">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="17d29-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="17d29-130">-VM</span><span class="sxs-lookup"><span data-stu-id="17d29-130">-VM</span></span>
<span data-ttu-id="17d29-131">Указывает локальный объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="17d29-132">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="17d29-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="17d29-133">Этот объект виртуальной машины включает обновленное состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="17d29-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="17d29-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17d29-134">-Confirm</span></span>
<span data-ttu-id="17d29-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17d29-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17d29-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d29-136">-WhatIf</span></span>
<span data-ttu-id="17d29-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17d29-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="17d29-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17d29-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17d29-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d29-139">CommonParameters</span></span>
<span data-ttu-id="17d29-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17d29-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d29-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17d29-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d29-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17d29-142">INPUTS</span></span>

## <span data-ttu-id="17d29-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17d29-143">OUTPUTS</span></span>

## <span data-ttu-id="17d29-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="17d29-144">NOTES</span></span>

## <span data-ttu-id="17d29-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17d29-145">RELATED LINKS</span></span>

[<span data-ttu-id="17d29-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="17d29-147">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="17d29-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="17d29-149">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="17d29-150">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="17d29-151">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="17d29-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="17d29-152">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="17d29-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


