---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 882b9f0afe9670f9e7b6f0651b3f3a96003d4668
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911564"
---
# <span data-ttu-id="67d49-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="67d49-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="67d49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67d49-102">SYNOPSIS</span></span>
<span data-ttu-id="67d49-103">Преобразует виртуальную машину с дисками на основе больших двоичных объектов на виртуальные машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="67d49-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="67d49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67d49-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67d49-105">DESCRIPTION</span></span>
<span data-ttu-id="67d49-106">Командлет **ConvertTo-AzVMManagedDisk** преобразует виртуальную машину с дисками, основанными на больших двоичных данных, в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="67d49-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="67d49-107">Перед вызовом этой операции виртуальная машина должна быть остановлена, пока она не будет выделена.</span><span class="sxs-lookup"><span data-stu-id="67d49-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="67d49-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67d49-108">EXAMPLES</span></span>

### <span data-ttu-id="67d49-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67d49-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="67d49-110">Эта команда преобразует диски на основе BLOB-объектов виртуальной машины с именем "VM01" в группу ресурсов "ResourceGroup01" на управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="67d49-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="67d49-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67d49-111">PARAMETERS</span></span>

### <span data-ttu-id="67d49-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d49-112">-AsJob</span></span>
<span data-ttu-id="67d49-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67d49-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d49-114">-DefaultProfile</span></span>
<span data-ttu-id="67d49-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67d49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d49-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d49-116">-ResourceGroupName</span></span>
<span data-ttu-id="67d49-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67d49-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="67d49-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="67d49-118">-VMName</span></span>
<span data-ttu-id="67d49-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67d49-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="67d49-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d49-120">-Confirm</span></span>
<span data-ttu-id="67d49-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67d49-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d49-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d49-122">-WhatIf</span></span>
<span data-ttu-id="67d49-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67d49-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67d49-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67d49-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d49-125">CommonParameters</span></span>
<span data-ttu-id="67d49-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67d49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d49-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d49-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d49-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67d49-128">INPUTS</span></span>

### <span data-ttu-id="67d49-129">System. String</span><span class="sxs-lookup"><span data-stu-id="67d49-129">System.String</span></span>

## <span data-ttu-id="67d49-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67d49-130">OUTPUTS</span></span>

### <span data-ttu-id="67d49-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="67d49-131">System.Object</span></span>

## <span data-ttu-id="67d49-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="67d49-132">NOTES</span></span>

## <span data-ttu-id="67d49-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67d49-133">RELATED LINKS</span></span>

