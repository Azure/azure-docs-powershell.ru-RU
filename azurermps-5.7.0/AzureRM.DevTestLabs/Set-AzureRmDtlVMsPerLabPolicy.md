---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 8e6e50fd22330073d647353232c549579aa382a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733063"
---
# <span data-ttu-id="2b623-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="2b623-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="2b623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b623-102">SYNOPSIS</span></span>
<span data-ttu-id="2b623-103">Задает виртуальные машины для каждой политики лаборатории лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="2b623-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b623-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b623-104">SYNTAX</span></span>

### <span data-ttu-id="2b623-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b623-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b623-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="2b623-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b623-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b623-107">DESCRIPTION</span></span>
<span data-ttu-id="2b623-108">Командлет **Set-AzureRmDtlVMsPerLabPolicy** задает виртуальные машины для каждой политики лаборатории лаборатории, которая задает общее количество виртуальных машин, разрешенных в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="2b623-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="2b623-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b623-110">EXAMPLES</span></span>

## <span data-ttu-id="2b623-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b623-111">PARAMETERS</span></span>

### <span data-ttu-id="2b623-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b623-112">-DefaultProfile</span></span>
<span data-ttu-id="2b623-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2b623-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b623-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="2b623-114">-Disable</span></span>
<span data-ttu-id="2b623-115">Указывает на то, что этот командлет отключает политику лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b623-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="2b623-116">-Enable</span></span>
<span data-ttu-id="2b623-117">Указывает на то, что этот командлет включает политику лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b623-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="2b623-118">-LabName</span></span>
<span data-ttu-id="2b623-119">Указывает имя лаборатории, для которой этот командлет задает виртуальные машины для каждой политики лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b623-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="2b623-120">-MaxVMs</span></span>
<span data-ttu-id="2b623-121">Указывает максимальное количество виртуальных машин, которые можно создать в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b623-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b623-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b623-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="2b623-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2b623-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b623-124">-Confirm</span></span>
<span data-ttu-id="2b623-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b623-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b623-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b623-126">-WhatIf</span></span>
<span data-ttu-id="2b623-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b623-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b623-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b623-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b623-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b623-129">CommonParameters</span></span>
<span data-ttu-id="2b623-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b623-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b623-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b623-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b623-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b623-132">INPUTS</span></span>

### <span data-ttu-id="2b623-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="2b623-133">None</span></span>
<span data-ttu-id="2b623-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2b623-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b623-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b623-135">OUTPUTS</span></span>

### <span data-ttu-id="2b623-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="2b623-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="2b623-137">Этот командлет возвращает политику, указывающую максимальное количество виртуальных машин, которые можно создать в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="2b623-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="2b623-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b623-138">NOTES</span></span>

## <span data-ttu-id="2b623-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b623-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b623-140">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="2b623-140">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


