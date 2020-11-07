---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
ms.openlocfilehash: 563b8acadcf84359af740f504f3b25555a2e45f1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914633"
---
# <span data-ttu-id="176f8-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="176f8-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="176f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="176f8-102">SYNOPSIS</span></span>
<span data-ttu-id="176f8-103">Преобразует виртуальную машину с дисками на основе больших двоичных объектов на виртуальные машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="176f8-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="176f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="176f8-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="176f8-105">DESCRIPTION</span></span>
<span data-ttu-id="176f8-106">Командлет **ConvertTo-AzureRmVMManagedDisk** преобразует виртуальную машину с дисками, основанными на больших двоичных данных, в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="176f8-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="176f8-107">Перед вызовом этой операции виртуальная машина должна быть остановлена, пока она не будет выделена.</span><span class="sxs-lookup"><span data-stu-id="176f8-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="176f8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="176f8-108">EXAMPLES</span></span>

### <span data-ttu-id="176f8-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="176f8-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="176f8-110">Эта команда преобразует диски на основе BLOB-объектов виртуальной машины с именем "VM01" в группу ресурсов "ResourceGroup01" на управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="176f8-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="176f8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="176f8-111">PARAMETERS</span></span>

### <span data-ttu-id="176f8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="176f8-112">-AsJob</span></span>
<span data-ttu-id="176f8-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="176f8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="176f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176f8-114">-DefaultProfile</span></span>
<span data-ttu-id="176f8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="176f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="176f8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176f8-116">-ResourceGroupName</span></span>
<span data-ttu-id="176f8-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176f8-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="176f8-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="176f8-118">-VMName</span></span>
<span data-ttu-id="176f8-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176f8-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="176f8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="176f8-120">-Confirm</span></span>
<span data-ttu-id="176f8-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="176f8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176f8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176f8-122">-WhatIf</span></span>
<span data-ttu-id="176f8-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="176f8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="176f8-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="176f8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176f8-125">CommonParameters</span></span>
<span data-ttu-id="176f8-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="176f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176f8-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176f8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176f8-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="176f8-128">INPUTS</span></span>

### <span data-ttu-id="176f8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="176f8-129">System.String</span></span>

## <span data-ttu-id="176f8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="176f8-130">OUTPUTS</span></span>

### <span data-ttu-id="176f8-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="176f8-131">System.Object</span></span>

## <span data-ttu-id="176f8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="176f8-132">NOTES</span></span>

## <span data-ttu-id="176f8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="176f8-133">RELATED LINKS</span></span>

