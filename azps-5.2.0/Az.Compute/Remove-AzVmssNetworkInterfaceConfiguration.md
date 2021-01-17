---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408012"
---
# <span data-ttu-id="03748-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="03748-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="03748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03748-102">SYNOPSIS</span></span>
<span data-ttu-id="03748-103">Удаляет конфигурацию сетевого интерфейса из VMSS.</span><span class="sxs-lookup"><span data-stu-id="03748-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="03748-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="03748-104">SYNTAX</span></span>

### <span data-ttu-id="03748-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="03748-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03748-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03748-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03748-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03748-107">DESCRIPTION</span></span>
<span data-ttu-id="03748-108">Командлет **Remove-AzVmssNetworkInterfaceConfiguration** удаляет конфигурацию сетевого интерфейса из набора масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="03748-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="03748-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="03748-109">EXAMPLES</span></span>

### <span data-ttu-id="03748-110">Пример 1. Удаление конфигурации интерфейса</span><span class="sxs-lookup"><span data-stu-id="03748-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="03748-111">Первая команда получает VMSS с Get-AzVmss командлетом, а затем сохраняет ее в $VMSS переменной.</span><span class="sxs-lookup"><span data-stu-id="03748-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="03748-112">Вторая команда удаляет конфигурацию сетевого интерфейса ContosoVmssInterface02 из набора в $VMSS.</span><span class="sxs-lookup"><span data-stu-id="03748-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="03748-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03748-113">PARAMETERS</span></span>

### <span data-ttu-id="03748-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03748-114">-DefaultProfile</span></span>
<span data-ttu-id="03748-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03748-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03748-116">-Id</span><span class="sxs-lookup"><span data-stu-id="03748-116">-Id</span></span>
<span data-ttu-id="03748-117">Определяет код конфигурации сетевого интерфейса, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03748-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-118">-Name</span><span class="sxs-lookup"><span data-stu-id="03748-118">-Name</span></span>
<span data-ttu-id="03748-119">Указывает имя конфигурации сетевого интерфейса, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03748-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="03748-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="03748-121">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="03748-121">Specifies the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03748-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03748-122">-Confirm</span></span>
<span data-ttu-id="03748-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03748-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03748-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03748-124">-WhatIf</span></span>
<span data-ttu-id="03748-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03748-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03748-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="03748-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03748-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03748-127">CommonParameters</span></span>
<span data-ttu-id="03748-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03748-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03748-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03748-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03748-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03748-130">INPUTS</span></span>

### <span data-ttu-id="03748-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="03748-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="03748-132">System.String</span><span class="sxs-lookup"><span data-stu-id="03748-132">System.String</span></span>

## <span data-ttu-id="03748-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03748-133">OUTPUTS</span></span>

### <span data-ttu-id="03748-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="03748-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="03748-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="03748-135">NOTES</span></span>

## <span data-ttu-id="03748-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03748-136">RELATED LINKS</span></span>

[<span data-ttu-id="03748-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="03748-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="03748-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="03748-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


