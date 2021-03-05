---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 33be258858a6ace456b7aa3c5b25594a373ccfd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013832"
---
# <span data-ttu-id="394e5-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="394e5-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="394e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="394e5-102">SYNOPSIS</span></span>
<span data-ttu-id="394e5-103">Свойства расширений виртуальной машины, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="394e5-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="394e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="394e5-104">SYNTAX</span></span>

### <span data-ttu-id="394e5-105">GetExtensionParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="394e5-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="394e5-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="394e5-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="394e5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="394e5-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="394e5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="394e5-108">DESCRIPTION</span></span>
<span data-ttu-id="394e5-109">Для получения свойств расширений виртуальной машины, установленных на виртуальной машине, возвращается cmdlet **Get-AzVMExtension.**</span><span class="sxs-lookup"><span data-stu-id="394e5-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="394e5-110">Укажите имя расширения, для которого нужно получить свойства.</span><span class="sxs-lookup"><span data-stu-id="394e5-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="394e5-111">Чтобы получить только представление экземпляра расширения, укажите параметр Status.</span><span class="sxs-lookup"><span data-stu-id="394e5-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="394e5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="394e5-112">EXAMPLES</span></span>

### <span data-ttu-id="394e5-113">Пример 1. Свойства расширения</span><span class="sxs-lookup"><span data-stu-id="394e5-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="394e5-114">Эта команда получает свойства расширения CustomScriptExtension на виртуальной машине с именем VirtualMa в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="394e5-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="394e5-115">Пример 2. Просмотр экземпляра расширения</span><span class="sxs-lookup"><span data-stu-id="394e5-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="394e5-116">Эта команда получает представление экземпляра расширения CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="394e5-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="394e5-117">Пример 3. Все расширения, установленные на VM-</span><span class="sxs-lookup"><span data-stu-id="394e5-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="394e5-118">Пример 4. Свойства расширения с помощью параметра VM</span><span class="sxs-lookup"><span data-stu-id="394e5-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="394e5-119">Эта команда получает список расширений, установленных на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="394e5-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="394e5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="394e5-120">PARAMETERS</span></span>

### <span data-ttu-id="394e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="394e5-121">-DefaultProfile</span></span>
<span data-ttu-id="394e5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="394e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="394e5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="394e5-123">-Name</span></span>
<span data-ttu-id="394e5-124">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="394e5-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="394e5-125">Этот cmdlet получает свойства для расширения, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="394e5-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="394e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="394e5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="394e5-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="394e5-128">-ResourceId</span></span>
<span data-ttu-id="394e5-129">ИД ресурса, задающий объект виртуальной машины, к объекту, на который указывает расширение.</span><span class="sxs-lookup"><span data-stu-id="394e5-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="394e5-130">-Status</span><span class="sxs-lookup"><span data-stu-id="394e5-130">-Status</span></span>
<span data-ttu-id="394e5-131">Указывает на то, что этот cmdlet получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="394e5-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e5-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="394e5-132">-VMName</span></span>
<span data-ttu-id="394e5-133">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="394e5-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="394e5-134">Этот cmdlet получает свойства расширения от виртуальной машины, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="394e5-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="394e5-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="394e5-135">-VMObject</span></span>
<span data-ttu-id="394e5-136">Определяет объект виртуальной машины, на который указывается расширение.</span><span class="sxs-lookup"><span data-stu-id="394e5-136">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="394e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394e5-137">CommonParameters</span></span>
<span data-ttu-id="394e5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="394e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394e5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="394e5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394e5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="394e5-140">INPUTS</span></span>

### <span data-ttu-id="394e5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="394e5-141">System.String</span></span>

### <span data-ttu-id="394e5-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="394e5-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="394e5-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="394e5-143">OUTPUTS</span></span>

### <span data-ttu-id="394e5-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="394e5-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="394e5-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="394e5-145">NOTES</span></span>

## <span data-ttu-id="394e5-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="394e5-146">RELATED LINKS</span></span>

[<span data-ttu-id="394e5-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="394e5-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="394e5-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="394e5-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


