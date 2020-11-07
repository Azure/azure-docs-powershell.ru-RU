---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 2fdbafba325d95f8e0ce2959e6f77c896dfa0722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721763"
---
# <span data-ttu-id="998e3-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="998e3-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="998e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="998e3-102">SYNOPSIS</span></span>
<span data-ttu-id="998e3-103">Удаляет обработчик расширений DSC из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="998e3-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="998e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="998e3-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="998e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="998e3-105">DESCRIPTION</span></span>
<span data-ttu-id="998e3-106">Командлет **Remove-AzVMDscExtension** удаляет обработчик расширения нужной конфигурации состояния (DSC) из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="998e3-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="998e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="998e3-107">EXAMPLES</span></span>

### <span data-ttu-id="998e3-108">Пример 1: удаление расширения DSC</span><span class="sxs-lookup"><span data-stu-id="998e3-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="998e3-109">Эта команда удаляет расширение с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="998e3-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="998e3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="998e3-110">PARAMETERS</span></span>

### <span data-ttu-id="998e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="998e3-111">-DefaultProfile</span></span>
<span data-ttu-id="998e3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="998e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="998e3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="998e3-113">-Name</span></span>
<span data-ttu-id="998e3-114">Указывает имя расширения DSC, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="998e3-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="998e3-115">Командлет Set-AzVMDscExtension задает это имя в Microsoft. PowerShell. DSC, которое является значением по умолчанию, используемым функцией **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="998e3-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998e3-116">-Wait</span><span class="sxs-lookup"><span data-stu-id="998e3-116">-NoWait</span></span>
<span data-ttu-id="998e3-117">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="998e3-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="998e3-118">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="998e3-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="998e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="998e3-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="998e3-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="998e3-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="998e3-121">-VMName</span></span>
<span data-ttu-id="998e3-122">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="998e3-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="998e3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="998e3-123">-Confirm</span></span>
<span data-ttu-id="998e3-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="998e3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="998e3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998e3-125">-WhatIf</span></span>
<span data-ttu-id="998e3-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="998e3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998e3-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="998e3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="998e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998e3-128">CommonParameters</span></span>
<span data-ttu-id="998e3-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="998e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998e3-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="998e3-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998e3-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="998e3-131">INPUTS</span></span>

### <span data-ttu-id="998e3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="998e3-132">System.String</span></span>

## <span data-ttu-id="998e3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="998e3-133">OUTPUTS</span></span>

### <span data-ttu-id="998e3-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="998e3-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="998e3-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="998e3-135">NOTES</span></span>

## <span data-ttu-id="998e3-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="998e3-136">RELATED LINKS</span></span>

[<span data-ttu-id="998e3-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="998e3-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="998e3-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="998e3-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


