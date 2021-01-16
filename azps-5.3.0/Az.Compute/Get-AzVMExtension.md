---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509170"
---
# <span data-ttu-id="f2bdf-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="f2bdf-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="f2bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bdf-103">Свойства расширений виртуальной машины, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="f2bdf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2bdf-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2bdf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bdf-106">Для получения свойств расширений виртуальной машины, установленных на виртуальной машине, возвращается cmdlet **Get-AzVMExtension.**</span><span class="sxs-lookup"><span data-stu-id="f2bdf-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="f2bdf-107">Укажите имя расширения, для которого нужно получить свойства.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="f2bdf-108">Чтобы получить только представление экземпляра расширения, укажите параметр Status.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="f2bdf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2bdf-109">EXAMPLES</span></span>

### <span data-ttu-id="f2bdf-110">Пример 1. Свойства расширения</span><span class="sxs-lookup"><span data-stu-id="f2bdf-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="f2bdf-111">Эта команда получает свойства расширения CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="f2bdf-112">Пример 2. Просмотр экземпляра расширения</span><span class="sxs-lookup"><span data-stu-id="f2bdf-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="f2bdf-113">Эта команда получает представление экземпляра расширения CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="f2bdf-114">Пример 3. Все расширения, установленные на VM-</span><span class="sxs-lookup"><span data-stu-id="f2bdf-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="f2bdf-115">Эта команда получает список расширений, установленных на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f2bdf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2bdf-116">PARAMETERS</span></span>

### <span data-ttu-id="f2bdf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bdf-117">-DefaultProfile</span></span>
<span data-ttu-id="f2bdf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2bdf-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f2bdf-119">-Name</span></span>
<span data-ttu-id="f2bdf-120">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="f2bdf-121">Этот cmdlet получает свойства для расширения, указанного этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2bdf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2bdf-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2bdf-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2bdf-124">-Status</span><span class="sxs-lookup"><span data-stu-id="f2bdf-124">-Status</span></span>
<span data-ttu-id="f2bdf-125">Указывает на то, что этот cmdlet получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="f2bdf-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2bdf-126">-VMName</span></span>
<span data-ttu-id="f2bdf-127">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f2bdf-128">Этот cmdlet получает свойства расширения от виртуальной машины, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2bdf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bdf-129">CommonParameters</span></span>
<span data-ttu-id="f2bdf-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2bdf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bdf-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2bdf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bdf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2bdf-132">INPUTS</span></span>

### <span data-ttu-id="f2bdf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f2bdf-133">System.String</span></span>

### <span data-ttu-id="f2bdf-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f2bdf-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f2bdf-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2bdf-135">OUTPUTS</span></span>

### <span data-ttu-id="f2bdf-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="f2bdf-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="f2bdf-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2bdf-137">NOTES</span></span>

## <span data-ttu-id="f2bdf-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2bdf-138">RELATED LINKS</span></span>

[<span data-ttu-id="f2bdf-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="f2bdf-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="f2bdf-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="f2bdf-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

