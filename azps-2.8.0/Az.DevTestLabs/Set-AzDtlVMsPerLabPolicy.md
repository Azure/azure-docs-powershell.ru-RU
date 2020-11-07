---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: d1a3cf7a70810babd17f222a9a7a72c141f8ec6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721072"
---
# <span data-ttu-id="9469b-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="9469b-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="9469b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9469b-102">SYNOPSIS</span></span>
<span data-ttu-id="9469b-103">Задает виртуальные машины для каждой политики лаборатории лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="9469b-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="9469b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9469b-104">SYNTAX</span></span>

### <span data-ttu-id="9469b-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9469b-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9469b-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="9469b-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9469b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9469b-107">DESCRIPTION</span></span>
<span data-ttu-id="9469b-108">Командлет **Set-AzDtlVMsPerLabPolicy** задает виртуальные машины для каждой политики лаборатории лаборатории, которая задает общее количество виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="9469b-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="9469b-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="9469b-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="9469b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9469b-110">EXAMPLES</span></span>

## <span data-ttu-id="9469b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9469b-111">PARAMETERS</span></span>

### <span data-ttu-id="9469b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9469b-112">-DefaultProfile</span></span>
<span data-ttu-id="9469b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9469b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9469b-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="9469b-114">-Disable</span></span>
<span data-ttu-id="9469b-115">Указывает на то, что этот командлет отключает политику лаборатории.</span><span class="sxs-lookup"><span data-stu-id="9469b-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="9469b-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="9469b-116">-Enable</span></span>
<span data-ttu-id="9469b-117">Указывает на то, что этот командлет включает политику лаборатории.</span><span class="sxs-lookup"><span data-stu-id="9469b-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="9469b-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="9469b-118">-LabName</span></span>
<span data-ttu-id="9469b-119">Указывает имя лаборатории, для которой этот командлет задает виртуальные машины для каждой политики лаборатории.</span><span class="sxs-lookup"><span data-stu-id="9469b-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="9469b-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="9469b-120">-MaxVMs</span></span>
<span data-ttu-id="9469b-121">Указывает максимальное количество виртуальных машин, которые можно создать в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="9469b-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9469b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9469b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9469b-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="9469b-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="9469b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9469b-124">-Confirm</span></span>
<span data-ttu-id="9469b-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9469b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9469b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9469b-126">-WhatIf</span></span>
<span data-ttu-id="9469b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9469b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9469b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9469b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9469b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9469b-129">CommonParameters</span></span>
<span data-ttu-id="9469b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9469b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9469b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9469b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9469b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9469b-132">INPUTS</span></span>

### <span data-ttu-id="9469b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9469b-133">System.String</span></span>

## <span data-ttu-id="9469b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9469b-134">OUTPUTS</span></span>

### <span data-ttu-id="9469b-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9469b-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="9469b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9469b-136">NOTES</span></span>

## <span data-ttu-id="9469b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9469b-137">RELATED LINKS</span></span>

[<span data-ttu-id="9469b-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="9469b-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


