---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8248c5ef5e4de2ab945d7f5f39dd4eea6defdf8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733738"
---
# <span data-ttu-id="83d5f-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="83d5f-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="83d5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83d5f-102">SYNOPSIS</span></span>
<span data-ttu-id="83d5f-103">Задает разрешенную политику размеров виртуальных машин для лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="83d5f-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83d5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83d5f-104">SYNTAX</span></span>

### <span data-ttu-id="83d5f-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83d5f-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83d5f-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="83d5f-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83d5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83d5f-107">DESCRIPTION</span></span>
<span data-ttu-id="83d5f-108">Командлет **Set-AzureRmDtlAllowedVMSizesPolicy** задает политику разрешенных размеров виртуальных машин, которая определяет список допустимых размеров виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="83d5f-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="83d5f-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="83d5f-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="83d5f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83d5f-110">EXAMPLES</span></span>

## <span data-ttu-id="83d5f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83d5f-111">PARAMETERS</span></span>

### <span data-ttu-id="83d5f-112">-Отключение</span><span class="sxs-lookup"><span data-stu-id="83d5f-112">-Disable</span></span>
<span data-ttu-id="83d5f-113">Указывает на то, что этот командлет отключает политику.</span><span class="sxs-lookup"><span data-stu-id="83d5f-113">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d5f-114">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="83d5f-114">-Enable</span></span>
<span data-ttu-id="83d5f-115">Указывает на то, что этот командлет включает политику.</span><span class="sxs-lookup"><span data-stu-id="83d5f-115">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d5f-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="83d5f-116">-LabName</span></span>
<span data-ttu-id="83d5f-117">Указывает имя лаборатории, для которой этот командлет задает политику размеров виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="83d5f-117">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="83d5f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d5f-118">-ResourceGroupName</span></span>
<span data-ttu-id="83d5f-119">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="83d5f-119">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="83d5f-120">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="83d5f-120">-VmSizes</span></span>
<span data-ttu-id="83d5f-121">Задает в качестве массива строк список размеров виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="83d5f-121">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d5f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83d5f-122">-Confirm</span></span>
<span data-ttu-id="83d5f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="83d5f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d5f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d5f-124">-WhatIf</span></span>
<span data-ttu-id="83d5f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="83d5f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d5f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="83d5f-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d5f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d5f-127">-DefaultProfile</span></span>
<span data-ttu-id="83d5f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83d5f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d5f-129">CommonParameters</span></span>
<span data-ttu-id="83d5f-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83d5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d5f-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d5f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d5f-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83d5f-132">INPUTS</span></span>

## <span data-ttu-id="83d5f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83d5f-133">OUTPUTS</span></span>

### <span data-ttu-id="83d5f-134">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="83d5f-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="83d5f-135">Этот командлет возвращает политику, которая определяет список размеров виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="83d5f-135">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="83d5f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="83d5f-136">NOTES</span></span>

## <span data-ttu-id="83d5f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83d5f-137">RELATED LINKS</span></span>

[<span data-ttu-id="83d5f-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="83d5f-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


