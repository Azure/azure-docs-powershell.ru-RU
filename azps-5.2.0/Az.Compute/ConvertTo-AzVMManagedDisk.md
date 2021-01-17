---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413175"
---
# <span data-ttu-id="65572-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="65572-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="65572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65572-102">SYNOPSIS</span></span>
<span data-ttu-id="65572-103">Преобразует виртуальную машину с дисками на основе BLOB-дисков в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="65572-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="65572-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65572-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65572-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65572-105">DESCRIPTION</span></span>
<span data-ttu-id="65572-106">Cmdlet **ConvertTo-AzVMManagedDisk** преобразует виртуальную машину с дисками на основе BLOB-дисков в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="65572-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="65572-107">Перед тем как делать это, нужно прекратить работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65572-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="65572-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65572-108">EXAMPLES</span></span>

### <span data-ttu-id="65572-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65572-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="65572-110">Эта команда преобразует диски виртуальной машины с именем "VM01" в группе ресурсов "Группа ресурсов" в управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="65572-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="65572-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65572-111">PARAMETERS</span></span>

### <span data-ttu-id="65572-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65572-112">-AsJob</span></span>
<span data-ttu-id="65572-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="65572-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65572-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65572-114">-DefaultProfile</span></span>
<span data-ttu-id="65572-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65572-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65572-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65572-116">-ResourceGroupName</span></span>
<span data-ttu-id="65572-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="65572-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="65572-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="65572-118">-VMName</span></span>
<span data-ttu-id="65572-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="65572-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="65572-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65572-120">-Confirm</span></span>
<span data-ttu-id="65572-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65572-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65572-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65572-122">-WhatIf</span></span>
<span data-ttu-id="65572-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65572-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65572-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="65572-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65572-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65572-125">CommonParameters</span></span>
<span data-ttu-id="65572-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65572-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65572-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65572-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65572-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65572-128">INPUTS</span></span>

### <span data-ttu-id="65572-129">System.String</span><span class="sxs-lookup"><span data-stu-id="65572-129">System.String</span></span>

## <span data-ttu-id="65572-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65572-130">OUTPUTS</span></span>

### <span data-ttu-id="65572-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="65572-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="65572-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65572-132">NOTES</span></span>

## <span data-ttu-id="65572-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65572-133">RELATED LINKS</span></span>
