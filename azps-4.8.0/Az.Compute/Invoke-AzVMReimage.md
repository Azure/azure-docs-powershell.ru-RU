---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235651"
---
# <span data-ttu-id="2fa5a-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2fa5a-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="2fa5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fa5a-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa5a-103">Переобразировать виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="2fa5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fa5a-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fa5a-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa5a-106">Командлет **Invoke-AzVMReimage** переобразует виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="2fa5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fa5a-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2fa5a-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2fa5a-109">Эта команда переобразует виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2fa5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fa5a-110">PARAMETERS</span></span>

### <span data-ttu-id="2fa5a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fa5a-111">-AsJob</span></span>
<span data-ttu-id="2fa5a-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2fa5a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fa5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa5a-113">-DefaultProfile</span></span>
<span data-ttu-id="2fa5a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fa5a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa5a-115">-ResourceGroupName</span></span>
<span data-ttu-id="2fa5a-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2fa5a-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="2fa5a-117">-TempDisk</span></span>
<span data-ttu-id="2fa5a-118">Указывает, следует ли переобразировать временный диск.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="2fa5a-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="2fa5a-119">-VMName</span></span>
<span data-ttu-id="2fa5a-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="2fa5a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fa5a-121">-Confirm</span></span>
<span data-ttu-id="2fa5a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa5a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa5a-123">-WhatIf</span></span>
<span data-ttu-id="2fa5a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa5a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa5a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa5a-126">CommonParameters</span></span>
<span data-ttu-id="2fa5a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fa5a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa5a-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fa5a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa5a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fa5a-129">INPUTS</span></span>

### <span data-ttu-id="2fa5a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa5a-130">System.String</span></span>

## <span data-ttu-id="2fa5a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fa5a-131">OUTPUTS</span></span>

### <span data-ttu-id="2fa5a-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2fa5a-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2fa5a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fa5a-133">NOTES</span></span>

## <span data-ttu-id="2fa5a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fa5a-134">RELATED LINKS</span></span>
