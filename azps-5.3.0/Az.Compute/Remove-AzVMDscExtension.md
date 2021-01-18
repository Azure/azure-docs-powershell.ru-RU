---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519515"
---
# <span data-ttu-id="04b9c-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="04b9c-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="04b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="04b9c-103">Удаляет обработчик расширения DSC с виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04b9c-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="04b9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04b9c-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04b9c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="04b9c-106">При этом из **виртуальной** машины в группе ресурсов удаляется обработчик расширения DSC .</span><span class="sxs-lookup"><span data-stu-id="04b9c-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="04b9c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="04b9c-108">Пример 1. Удаление расширения DSC</span><span class="sxs-lookup"><span data-stu-id="04b9c-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="04b9c-109">Эта команда удаляет расширение DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="04b9c-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="04b9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04b9c-110">PARAMETERS</span></span>

### <span data-ttu-id="04b9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b9c-111">-DefaultProfile</span></span>
<span data-ttu-id="04b9c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04b9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04b9c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="04b9c-113">-Name</span></span>
<span data-ttu-id="04b9c-114">Указывает имя расширения DSC, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b9c-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="04b9c-115">Этот Set-AzVMDscExtension задает это имя Microsoft.Powershell.DSC, которое используется по умолчанию для **remove-AzVMDscExtension.**</span><span class="sxs-lookup"><span data-stu-id="04b9c-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

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

### <span data-ttu-id="04b9c-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="04b9c-116">-NoWait</span></span>
<span data-ttu-id="04b9c-117">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="04b9c-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="04b9c-118">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="04b9c-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="04b9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04b9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="04b9c-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="04b9c-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="04b9c-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="04b9c-121">-VMName</span></span>
<span data-ttu-id="04b9c-122">Указывает имя виртуальной машины, с которой этот cmdlet удаляет расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="04b9c-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="04b9c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04b9c-123">-Confirm</span></span>
<span data-ttu-id="04b9c-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04b9c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04b9c-125">-WhatIf</span></span>
<span data-ttu-id="04b9c-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04b9c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04b9c-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="04b9c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04b9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b9c-128">CommonParameters</span></span>
<span data-ttu-id="04b9c-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b9c-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04b9c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b9c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04b9c-131">INPUTS</span></span>

### <span data-ttu-id="04b9c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="04b9c-132">System.String</span></span>

## <span data-ttu-id="04b9c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04b9c-133">OUTPUTS</span></span>

### <span data-ttu-id="04b9c-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04b9c-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="04b9c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04b9c-135">NOTES</span></span>

## <span data-ttu-id="04b9c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04b9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="04b9c-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="04b9c-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="04b9c-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="04b9c-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


