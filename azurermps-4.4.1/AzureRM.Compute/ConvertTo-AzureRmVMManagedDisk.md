---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 6931f6d80d3e279259b599b782a505b2a21dd074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569663"
---
# <span data-ttu-id="7c5e1-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7c5e1-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="7c5e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5e1-103">Преобразует виртуальную машину с дисками на основе больших двоичных объектов на виртуальные машины с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c5e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c5e1-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c5e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c5e1-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5e1-106">Командлет **ConvertTo-AzureRmVMManagedDisk** преобразует виртуальную машину с дисками, основанными на больших двоичных данных, в виртуальную машину с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="7c5e1-107">Перед вызовом этой операции виртуальная машина должна быть остановлена, пока она не будет выделена.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="7c5e1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c5e1-108">EXAMPLES</span></span>

### <span data-ttu-id="7c5e1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c5e1-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="7c5e1-110">Эта команда преобразует диски на основе BLOB-объектов виртуальной машины с именем "VM01" в группу ресурсов "ResourceGroup01" на управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="7c5e1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c5e1-111">PARAMETERS</span></span>

### <span data-ttu-id="7c5e1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5e1-112">-DefaultProfile</span></span>
<span data-ttu-id="7c5e1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c5e1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5e1-114">-ResourceGroupName</span></span>
<span data-ttu-id="7c5e1-115">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7c5e1-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c5e1-116">-VMName</span></span>
<span data-ttu-id="7c5e1-117">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7c5e1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c5e1-118">-Confirm</span></span>
<span data-ttu-id="7c5e1-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c5e1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c5e1-120">-WhatIf</span></span>
<span data-ttu-id="7c5e1-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c5e1-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c5e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5e1-123">CommonParameters</span></span>
<span data-ttu-id="7c5e1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c5e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5e1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c5e1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5e1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c5e1-126">INPUTS</span></span>

### <span data-ttu-id="7c5e1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7c5e1-127">System.String</span></span>

## <span data-ttu-id="7c5e1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c5e1-128">OUTPUTS</span></span>

### <span data-ttu-id="7c5e1-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="7c5e1-129">System.Object</span></span>

## <span data-ttu-id="7c5e1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c5e1-130">NOTES</span></span>

## <span data-ttu-id="7c5e1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c5e1-131">RELATED LINKS</span></span>

