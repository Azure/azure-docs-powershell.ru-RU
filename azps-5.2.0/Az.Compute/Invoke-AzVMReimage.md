---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415852"
---
# <span data-ttu-id="bbca0-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="bbca0-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="bbca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbca0-102">SYNOPSIS</span></span>
<span data-ttu-id="bbca0-103">Повторное использование виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="bbca0-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="bbca0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bbca0-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbca0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbca0-105">DESCRIPTION</span></span>
<span data-ttu-id="bbca0-106">**Cmdlet Invoke-AzVMReimage** повторно вызывает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="bbca0-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="bbca0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bbca0-107">EXAMPLES</span></span>

### <span data-ttu-id="bbca0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbca0-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="bbca0-109">Эта команда переимежает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bbca0-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="bbca0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbca0-110">PARAMETERS</span></span>

### <span data-ttu-id="bbca0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbca0-111">-AsJob</span></span>
<span data-ttu-id="bbca0-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bbca0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbca0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbca0-113">-DefaultProfile</span></span>
<span data-ttu-id="bbca0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbca0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbca0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbca0-115">-ResourceGroupName</span></span>
<span data-ttu-id="bbca0-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bbca0-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bbca0-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="bbca0-117">-TempDisk</span></span>
<span data-ttu-id="bbca0-118">Указывает, нужно ли повторно реимять диск temp.</span><span class="sxs-lookup"><span data-stu-id="bbca0-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="bbca0-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="bbca0-119">-VMName</span></span>
<span data-ttu-id="bbca0-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bbca0-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="bbca0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbca0-121">-Confirm</span></span>
<span data-ttu-id="bbca0-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbca0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbca0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbca0-123">-WhatIf</span></span>
<span data-ttu-id="bbca0-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbca0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbca0-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bbca0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbca0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbca0-126">CommonParameters</span></span>
<span data-ttu-id="bbca0-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbca0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbca0-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbca0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbca0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbca0-129">INPUTS</span></span>

### <span data-ttu-id="bbca0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bbca0-130">System.String</span></span>

## <span data-ttu-id="bbca0-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bbca0-131">OUTPUTS</span></span>

### <span data-ttu-id="bbca0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bbca0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bbca0-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bbca0-133">NOTES</span></span>

## <span data-ttu-id="bbca0-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbca0-134">RELATED LINKS</span></span>
