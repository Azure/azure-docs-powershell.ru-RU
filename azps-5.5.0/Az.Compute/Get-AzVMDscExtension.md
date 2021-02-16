---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: e487e86c26ec09d1335ee34dab56292b564169b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233388"
---
# <span data-ttu-id="ae624-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae624-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="ae624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae624-102">SYNOPSIS</span></span>
<span data-ttu-id="ae624-103">Получает параметры расширения DSC на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ae624-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="ae624-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae624-104">SYNTAX</span></span>

### <span data-ttu-id="ae624-105">GetDscExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae624-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae624-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae624-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae624-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae624-107">DESCRIPTION</span></span>
<span data-ttu-id="ae624-108">Для **параметра Get-AzVMDscExtension** задаются параметры расширения DSC на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ae624-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="ae624-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae624-109">EXAMPLES</span></span>

### <span data-ttu-id="ae624-110">Пример 1. Настройка расширения DSC</span><span class="sxs-lookup"><span data-stu-id="ae624-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="ae624-111">Эта команда получает параметры расширения DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="ae624-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="ae624-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae624-112">PARAMETERS</span></span>

### <span data-ttu-id="ae624-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae624-113">-DefaultProfile</span></span>
<span data-ttu-id="ae624-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae624-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae624-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ae624-115">-Name</span></span>
<span data-ttu-id="ae624-116">Имя ресурса Диспетчера ресурсов Azure, представляюца расширение.</span><span class="sxs-lookup"><span data-stu-id="ae624-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="ae624-117">Этот Set-AzVMDscExtension задает это имя Microsoft.Powershell.DSC, то есть то же значение, которое используется **в get-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="ae624-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="ae624-118">Укажите этот параметр только в том случае, если вы изменили имя по умолчанию в проектлете **Set-AzVMDscExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae624-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae624-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae624-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae624-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ae624-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae624-121">-Status</span><span class="sxs-lookup"><span data-stu-id="ae624-121">-Status</span></span>
<span data-ttu-id="ae624-122">Указывает на то, что этот cmdlet получает представление экземпляра расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="ae624-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae624-123">-VM</span><span class="sxs-lookup"><span data-stu-id="ae624-123">-VM</span></span>
<span data-ttu-id="ae624-124">Определяет объект виртуальной машины, на который указывается расширение.</span><span class="sxs-lookup"><span data-stu-id="ae624-124">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="ae624-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="ae624-125">-VMName</span></span>
<span data-ttu-id="ae624-126">Указывает имя виртуальной машины, для которой этот cmdlet получает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="ae624-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae624-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae624-127">CommonParameters</span></span>
<span data-ttu-id="ae624-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae624-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae624-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae624-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae624-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae624-130">INPUTS</span></span>

### <span data-ttu-id="ae624-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ae624-131">System.String</span></span>

### <span data-ttu-id="ae624-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae624-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae624-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae624-133">OUTPUTS</span></span>

### <span data-ttu-id="ae624-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ae624-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="ae624-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae624-135">NOTES</span></span>

## <span data-ttu-id="ae624-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae624-136">RELATED LINKS</span></span>

[<span data-ttu-id="ae624-137">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae624-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="ae624-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae624-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


