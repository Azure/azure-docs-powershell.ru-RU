---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065955"
---
# <span data-ttu-id="4f005-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4f005-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="4f005-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f005-102">SYNOPSIS</span></span>
<span data-ttu-id="4f005-103">Переобразировать виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="4f005-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="4f005-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f005-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f005-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f005-105">DESCRIPTION</span></span>
<span data-ttu-id="4f005-106">Командлет **Invoke-AzVMReimage** переобразует виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="4f005-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="4f005-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f005-107">EXAMPLES</span></span>

### <span data-ttu-id="4f005-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f005-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="4f005-109">Эта команда переобразует виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4f005-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="4f005-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f005-110">PARAMETERS</span></span>

### <span data-ttu-id="4f005-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f005-111">-AsJob</span></span>
<span data-ttu-id="4f005-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4f005-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f005-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f005-113">-DefaultProfile</span></span>
<span data-ttu-id="4f005-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f005-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f005-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f005-115">-ResourceGroupName</span></span>
<span data-ttu-id="4f005-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f005-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4f005-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="4f005-117">-TempDisk</span></span>
<span data-ttu-id="4f005-118">Указывает, следует ли переобразировать временный диск.</span><span class="sxs-lookup"><span data-stu-id="4f005-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="4f005-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="4f005-119">-VMName</span></span>
<span data-ttu-id="4f005-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4f005-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="4f005-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f005-121">-Confirm</span></span>
<span data-ttu-id="4f005-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4f005-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f005-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f005-123">-WhatIf</span></span>
<span data-ttu-id="4f005-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4f005-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f005-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f005-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f005-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f005-126">CommonParameters</span></span>
<span data-ttu-id="4f005-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f005-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f005-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f005-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f005-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f005-129">INPUTS</span></span>

### <span data-ttu-id="4f005-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4f005-130">System.String</span></span>

## <span data-ttu-id="4f005-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f005-131">OUTPUTS</span></span>

### <span data-ttu-id="4f005-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4f005-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4f005-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f005-133">NOTES</span></span>

## <span data-ttu-id="4f005-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f005-134">RELATED LINKS</span></span>
