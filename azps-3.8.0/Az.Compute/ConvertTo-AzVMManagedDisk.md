---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 2436874c58a5d8865dc29ffb29cde8397e7389e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912898"
---
# <span data-ttu-id="8b7ec-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8b7ec-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="8b7ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7ec-103">Преобразует виртуальную машину с дисками на основе больших двоичных объектов на виртуальные машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="8b7ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b7ec-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="8b7ec-106">Командлет **ConvertTo-AzVMManagedDisk** преобразует виртуальную машину с дисками, основанными на больших двоичных данных, в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="8b7ec-107">Перед вызовом этой операции виртуальная машина должна быть остановлена, пока она не будет выделена.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="8b7ec-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b7ec-108">EXAMPLES</span></span>

### <span data-ttu-id="8b7ec-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b7ec-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="8b7ec-110">Эта команда преобразует диски на основе BLOB-объектов виртуальной машины с именем "VM01" в группу ресурсов "ResourceGroup01" на управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="8b7ec-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b7ec-111">PARAMETERS</span></span>

### <span data-ttu-id="8b7ec-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b7ec-112">-AsJob</span></span>
<span data-ttu-id="8b7ec-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b7ec-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b7ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7ec-114">-DefaultProfile</span></span>
<span data-ttu-id="8b7ec-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b7ec-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b7ec-116">-ResourceGroupName</span></span>
<span data-ttu-id="8b7ec-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b7ec-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b7ec-118">-VMName</span></span>
<span data-ttu-id="8b7ec-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8b7ec-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b7ec-120">-Confirm</span></span>
<span data-ttu-id="8b7ec-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b7ec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7ec-122">-WhatIf</span></span>
<span data-ttu-id="8b7ec-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b7ec-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b7ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7ec-125">CommonParameters</span></span>
<span data-ttu-id="8b7ec-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b7ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7ec-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b7ec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7ec-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b7ec-128">INPUTS</span></span>

### <span data-ttu-id="8b7ec-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8b7ec-129">System.String</span></span>

## <span data-ttu-id="8b7ec-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b7ec-130">OUTPUTS</span></span>

### <span data-ttu-id="8b7ec-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8b7ec-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8b7ec-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b7ec-132">NOTES</span></span>

## <span data-ttu-id="8b7ec-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b7ec-133">RELATED LINKS</span></span>
