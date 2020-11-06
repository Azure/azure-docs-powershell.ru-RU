---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568634"
---
# <span data-ttu-id="2f413-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2f413-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="2f413-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f413-102">SYNOPSIS</span></span>
<span data-ttu-id="2f413-103">Преобразует виртуальную машину с дисками на основе больших двоичных объектов на виртуальные машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="2f413-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f413-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f413-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f413-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f413-105">DESCRIPTION</span></span>
<span data-ttu-id="2f413-106">Командлет **ConvertTo-AzureRmVMManagedDisk** преобразует виртуальную машину с дисками, основанными на больших двоичных данных, в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="2f413-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="2f413-107">Перед вызовом этой операции виртуальная машина должна быть остановлена, пока она не будет выделена.</span><span class="sxs-lookup"><span data-stu-id="2f413-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="2f413-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f413-108">EXAMPLES</span></span>

### <span data-ttu-id="2f413-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2f413-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="2f413-110">Эта команда преобразует диски на основе BLOB-объектов виртуальной машины с именем "VM01" в группу ресурсов "ResourceGroup01" на управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="2f413-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="2f413-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f413-111">PARAMETERS</span></span>

### <span data-ttu-id="2f413-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f413-112">-ResourceGroupName</span></span>
<span data-ttu-id="2f413-113">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f413-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f413-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="2f413-114">-VMName</span></span>
<span data-ttu-id="2f413-115">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f413-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f413-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f413-116">-Confirm</span></span>
<span data-ttu-id="2f413-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f413-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f413-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f413-118">-WhatIf</span></span>
<span data-ttu-id="2f413-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f413-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f413-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f413-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f413-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f413-121">CommonParameters</span></span>
<span data-ttu-id="2f413-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f413-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f413-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f413-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f413-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f413-124">INPUTS</span></span>

### <span data-ttu-id="2f413-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2f413-125">System.String</span></span>

## <span data-ttu-id="2f413-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f413-126">OUTPUTS</span></span>

### <span data-ttu-id="2f413-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="2f413-127">System.Object</span></span>

## <span data-ttu-id="2f413-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f413-128">NOTES</span></span>

## <span data-ttu-id="2f413-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f413-129">RELATED LINKS</span></span>

