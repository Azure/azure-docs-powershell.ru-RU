---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066861"
---
# <span data-ttu-id="575b6-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="575b6-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="575b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="575b6-102">SYNOPSIS</span></span>
<span data-ttu-id="575b6-103">Задает разрешенную политику размеров виртуальных машин для лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="575b6-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="575b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="575b6-104">SYNTAX</span></span>

### <span data-ttu-id="575b6-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="575b6-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="575b6-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="575b6-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="575b6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="575b6-107">DESCRIPTION</span></span>
<span data-ttu-id="575b6-108">Командлет **Set-AzDtlAllowedVMSizesPolicy** задает политику разрешенных размеров виртуальных машин, которая определяет список допустимых размеров виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="575b6-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="575b6-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="575b6-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="575b6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="575b6-110">EXAMPLES</span></span>

## <span data-ttu-id="575b6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="575b6-111">PARAMETERS</span></span>

### <span data-ttu-id="575b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575b6-112">-DefaultProfile</span></span>
<span data-ttu-id="575b6-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="575b6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="575b6-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="575b6-114">-Disable</span></span>
<span data-ttu-id="575b6-115">Указывает на то, что этот командлет отключает политику.</span><span class="sxs-lookup"><span data-stu-id="575b6-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="575b6-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="575b6-116">-Enable</span></span>
<span data-ttu-id="575b6-117">Указывает на то, что этот командлет включает политику.</span><span class="sxs-lookup"><span data-stu-id="575b6-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="575b6-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="575b6-118">-LabName</span></span>
<span data-ttu-id="575b6-119">Указывает имя лаборатории, для которой этот командлет задает политику размеров виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="575b6-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="575b6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575b6-120">-ResourceGroupName</span></span>
<span data-ttu-id="575b6-121">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="575b6-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="575b6-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="575b6-122">-VmSizes</span></span>
<span data-ttu-id="575b6-123">Задает в качестве массива строк список размеров виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="575b6-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="575b6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="575b6-124">-Confirm</span></span>
<span data-ttu-id="575b6-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="575b6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="575b6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575b6-126">-WhatIf</span></span>
<span data-ttu-id="575b6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="575b6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575b6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="575b6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="575b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575b6-129">CommonParameters</span></span>
<span data-ttu-id="575b6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="575b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575b6-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575b6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575b6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="575b6-132">INPUTS</span></span>

### <span data-ttu-id="575b6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="575b6-133">System.String</span></span>

## <span data-ttu-id="575b6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="575b6-134">OUTPUTS</span></span>

### <span data-ttu-id="575b6-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="575b6-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="575b6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="575b6-136">NOTES</span></span>

## <span data-ttu-id="575b6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="575b6-137">RELATED LINKS</span></span>

[<span data-ttu-id="575b6-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="575b6-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


