---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079102"
---
# <span data-ttu-id="1cb70-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1cb70-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="1cb70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cb70-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb70-103">Удаляет конфигурацию сетевого интерфейса из VMSS.</span><span class="sxs-lookup"><span data-stu-id="1cb70-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="1cb70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cb70-104">SYNTAX</span></span>

### <span data-ttu-id="1cb70-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb70-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb70-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb70-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb70-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb70-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb70-108">Командлет **Remove-AzVmssNetworkInterfaceConfiguration** удаляет конфигурацию сетевого интерфейса из установленной шкалы виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1cb70-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1cb70-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cb70-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb70-110">Пример 1: Удаление конфигурации интерфейса</span><span class="sxs-lookup"><span data-stu-id="1cb70-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="1cb70-111">Первая команда получает объект VMSS с помощью командлета Get-AzVmss и сохраняет его в переменной $VMSS.</span><span class="sxs-lookup"><span data-stu-id="1cb70-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="1cb70-112">Вторая команда удаляет конфигурацию сетевого интерфейса с именем ContosoVmssInterface02 из комплекта в $VMSS.</span><span class="sxs-lookup"><span data-stu-id="1cb70-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="1cb70-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cb70-113">PARAMETERS</span></span>

### <span data-ttu-id="1cb70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb70-114">-DefaultProfile</span></span>
<span data-ttu-id="1cb70-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb70-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb70-116">-ID</span><span class="sxs-lookup"><span data-stu-id="1cb70-116">-Id</span></span>
<span data-ttu-id="1cb70-117">Указывает идентификатор конфигурации сетевого интерфейса, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1cb70-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1cb70-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cb70-118">-Name</span></span>
<span data-ttu-id="1cb70-119">Указывает имя конфигурации сетевого интерфейса, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1cb70-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1cb70-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1cb70-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1cb70-121">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="1cb70-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="1cb70-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cb70-122">-Confirm</span></span>
<span data-ttu-id="1cb70-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1cb70-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb70-124">-WhatIf</span></span>
<span data-ttu-id="1cb70-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1cb70-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cb70-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1cb70-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb70-127">CommonParameters</span></span>
<span data-ttu-id="1cb70-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cb70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb70-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cb70-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb70-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cb70-130">INPUTS</span></span>

### <span data-ttu-id="1cb70-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1cb70-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1cb70-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb70-132">System.String</span></span>

## <span data-ttu-id="1cb70-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb70-133">OUTPUTS</span></span>

### <span data-ttu-id="1cb70-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1cb70-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1cb70-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cb70-135">NOTES</span></span>

## <span data-ttu-id="1cb70-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cb70-136">RELATED LINKS</span></span>

[<span data-ttu-id="1cb70-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1cb70-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="1cb70-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="1cb70-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


