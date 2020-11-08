---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingosupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingOSUpgrade.md
ms.openlocfilehash: ad5d387a0935150a66924cbfdd19ac40ed57079c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079098"
---
# <span data-ttu-id="40bb3-101">Start-AzVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="40bb3-101">Start-AzVmssRollingOSUpgrade</span></span>

## <span data-ttu-id="40bb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="40bb3-103">Запускает чередующееся обновление, чтобы переместить все экземпляры наборов масштабов виртуальных машин в последнюю доступную версию ОС образа платформы.</span><span class="sxs-lookup"><span data-stu-id="40bb3-103">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>

## <span data-ttu-id="40bb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40bb3-104">SYNTAX</span></span>

```
Start-AzVmssRollingOSUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40bb3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="40bb3-106">Запускает чередующееся обновление, чтобы переместить все экземпляры наборов масштабов виртуальных машин в последнюю доступную версию ОС образа платформы.</span><span class="sxs-lookup"><span data-stu-id="40bb3-106">Starts a rolling upgrade to move all virtual machine scale set instances to the latest available Platform Image OS version.</span></span>
<span data-ttu-id="40bb3-107">Для экземпляров, уже использующих последнюю доступную версию операционной системы, это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="40bb3-107">Instances which are already running the latest available OS version are not affected.</span></span>

## <span data-ttu-id="40bb3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40bb3-108">EXAMPLES</span></span>

### <span data-ttu-id="40bb3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40bb3-109">Example 1</span></span>
```
PS C:\> Start-AzVmssRollingOSUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="40bb3-110">Эта команда запускает чередующееся обновление всех экземпляров виртуальной машины, установленной на "VMSS001" в группе ресурсов "Group001".</span><span class="sxs-lookup"><span data-stu-id="40bb3-110">This command starts a rolling upgrade of all vm instances of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="40bb3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40bb3-111">PARAMETERS</span></span>

### <span data-ttu-id="40bb3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40bb3-112">-AsJob</span></span>
<span data-ttu-id="40bb3-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="40bb3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40bb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bb3-114">-DefaultProfile</span></span>
<span data-ttu-id="40bb3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40bb3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40bb3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bb3-116">-ResourceGroupName</span></span>
<span data-ttu-id="40bb3-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40bb3-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="40bb3-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="40bb3-118">-VMScaleSetName</span></span>
<span data-ttu-id="40bb3-119">Имя набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="40bb3-119">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40bb3-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40bb3-120">-Confirm</span></span>
<span data-ttu-id="40bb3-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40bb3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bb3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bb3-122">-WhatIf</span></span>
<span data-ttu-id="40bb3-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40bb3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bb3-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40bb3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bb3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bb3-125">CommonParameters</span></span>
<span data-ttu-id="40bb3-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40bb3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bb3-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40bb3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bb3-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40bb3-128">INPUTS</span></span>

### <span data-ttu-id="40bb3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="40bb3-129">System.String</span></span>

## <span data-ttu-id="40bb3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40bb3-130">OUTPUTS</span></span>

### <span data-ttu-id="40bb3-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="40bb3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="40bb3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="40bb3-132">NOTES</span></span>

## <span data-ttu-id="40bb3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40bb3-133">RELATED LINKS</span></span>
