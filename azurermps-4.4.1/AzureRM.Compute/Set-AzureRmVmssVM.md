---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559943"
---
# <span data-ttu-id="5ff5c-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="5ff5c-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="5ff5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ff5c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff5c-103">Изменяет состояние экземпляра VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ff5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ff5c-104">SYNTAX</span></span>

### <span data-ttu-id="5ff5c-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ff5c-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ff5c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="5ff5c-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff5c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ff5c-107">DESCRIPTION</span></span>
<span data-ttu-id="5ff5c-108">Командлет **Set-AzureRmVmssVM** изменяет состояние экземпляра набора масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5ff5c-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="5ff5c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ff5c-109">EXAMPLES</span></span>

## <span data-ttu-id="5ff5c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ff5c-110">PARAMETERS</span></span>

### <span data-ttu-id="5ff5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff5c-111">-DefaultProfile</span></span>
<span data-ttu-id="5ff5c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ff5c-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="5ff5c-113">-InstanceId</span></span>
<span data-ttu-id="5ff5c-114">Указывает идентификатор экземпляра VMSS, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff5c-115">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="5ff5c-115">-Reimage</span></span>
<span data-ttu-id="5ff5c-116">Указывает на то, что этот командлет переобразировать экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff5c-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="5ff5c-117">-ReimageAll</span></span>
<span data-ttu-id="5ff5c-118">Указывает, что командлет переобразует все диски в экземпляре VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff5c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ff5c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5ff5c-120">Указывает имя группы ресурсов, которая содержит экземпляр VMSS.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="5ff5c-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="5ff5c-121">-VMScaleSetName</span></span>
<span data-ttu-id="5ff5c-122">Указывает имя экземпляра VMSS, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5ff5c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ff5c-123">-Confirm</span></span>
<span data-ttu-id="5ff5c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff5c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff5c-125">-WhatIf</span></span>
<span data-ttu-id="5ff5c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ff5c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff5c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff5c-128">CommonParameters</span></span>
<span data-ttu-id="5ff5c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ff5c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff5c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff5c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff5c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ff5c-131">INPUTS</span></span>

## <span data-ttu-id="5ff5c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ff5c-132">OUTPUTS</span></span>

## <span data-ttu-id="5ff5c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ff5c-133">NOTES</span></span>

## <span data-ttu-id="5ff5c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ff5c-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ff5c-135">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="5ff5c-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
