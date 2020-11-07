---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 4aabd2a7b6e8b4b0b9037fc14189a0e14fdf8920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732798"
---
# <span data-ttu-id="1fc64-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1fc64-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="1fc64-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fc64-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc64-103">Преобразует виртуальную машину с дисками на основе больших двоичных объектов на виртуальные машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="1fc64-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fc64-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fc64-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc64-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc64-105">DESCRIPTION</span></span>
<span data-ttu-id="1fc64-106">Командлет **ConvertTo-AzureRmVMManagedDisk** преобразует виртуальную машину с дисками, основанными на больших двоичных данных, в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="1fc64-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="1fc64-107">Перед вызовом этой операции виртуальная машина должна быть остановлена, пока она не будет выделена.</span><span class="sxs-lookup"><span data-stu-id="1fc64-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="1fc64-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fc64-108">EXAMPLES</span></span>

### <span data-ttu-id="1fc64-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fc64-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="1fc64-110">Эта команда преобразует диски на основе BLOB-объектов виртуальной машины с именем "VM01" в группу ресурсов "ResourceGroup01" на управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="1fc64-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="1fc64-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fc64-111">PARAMETERS</span></span>

### <span data-ttu-id="1fc64-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fc64-112">-AsJob</span></span>
<span data-ttu-id="1fc64-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1fc64-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fc64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc64-114">-DefaultProfile</span></span>
<span data-ttu-id="1fc64-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fc64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fc64-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc64-116">-ResourceGroupName</span></span>
<span data-ttu-id="1fc64-117">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fc64-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1fc64-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="1fc64-118">-VMName</span></span>
<span data-ttu-id="1fc64-119">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1fc64-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc64-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fc64-120">-Confirm</span></span>
<span data-ttu-id="1fc64-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fc64-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc64-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc64-122">-WhatIf</span></span>
<span data-ttu-id="1fc64-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fc64-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fc64-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fc64-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc64-125">CommonParameters</span></span>
<span data-ttu-id="1fc64-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fc64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc64-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc64-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc64-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fc64-128">INPUTS</span></span>

### <span data-ttu-id="1fc64-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1fc64-129">System.String</span></span>

## <span data-ttu-id="1fc64-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc64-130">OUTPUTS</span></span>

### <span data-ttu-id="1fc64-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1fc64-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1fc64-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fc64-132">NOTES</span></span>

## <span data-ttu-id="1fc64-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fc64-133">RELATED LINKS</span></span>
