---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245543"
---
# <span data-ttu-id="ae0dd-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ae0dd-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="ae0dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae0dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0dd-103">Задает разрешенную политику размеров виртуальных машин для лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ae0dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae0dd-104">SYNTAX</span></span>

### <span data-ttu-id="ae0dd-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae0dd-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae0dd-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="ae0dd-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae0dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0dd-107">DESCRIPTION</span></span>
<span data-ttu-id="ae0dd-108">Командлет **Set-AzDtlAllowedVMSizesPolicy** задает политику разрешенных размеров виртуальных машин, которая определяет список допустимых размеров виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="ae0dd-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="ae0dd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae0dd-110">EXAMPLES</span></span>

## <span data-ttu-id="ae0dd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae0dd-111">PARAMETERS</span></span>

### <span data-ttu-id="ae0dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0dd-112">-DefaultProfile</span></span>
<span data-ttu-id="ae0dd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae0dd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae0dd-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="ae0dd-114">-Disable</span></span>
<span data-ttu-id="ae0dd-115">Указывает на то, что этот командлет отключает политику.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0dd-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="ae0dd-116">-Enable</span></span>
<span data-ttu-id="ae0dd-117">Указывает на то, что этот командлет включает политику.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0dd-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="ae0dd-118">-LabName</span></span>
<span data-ttu-id="ae0dd-119">Указывает имя лаборатории, для которой этот командлет задает политику размеров виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="ae0dd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0dd-120">-ResourceGroupName</span></span>
<span data-ttu-id="ae0dd-121">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ae0dd-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="ae0dd-122">-VmSizes</span></span>
<span data-ttu-id="ae0dd-123">Задает в качестве массива строк список размеров виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae0dd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae0dd-124">-Confirm</span></span>
<span data-ttu-id="ae0dd-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae0dd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0dd-126">-WhatIf</span></span>
<span data-ttu-id="ae0dd-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0dd-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae0dd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0dd-129">CommonParameters</span></span>
<span data-ttu-id="ae0dd-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae0dd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0dd-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae0dd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0dd-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae0dd-132">INPUTS</span></span>

### <span data-ttu-id="ae0dd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ae0dd-133">System.String</span></span>

## <span data-ttu-id="ae0dd-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0dd-134">OUTPUTS</span></span>

### <span data-ttu-id="ae0dd-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ae0dd-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ae0dd-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae0dd-136">NOTES</span></span>

## <span data-ttu-id="ae0dd-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae0dd-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae0dd-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ae0dd-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)

