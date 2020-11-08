---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245537"
---
# <span data-ttu-id="dcfe7-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="dcfe7-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="dcfe7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcfe7-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfe7-103">Задает политику виртуальных машин на пользователя лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="dcfe7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcfe7-104">SYNTAX</span></span>

### <span data-ttu-id="dcfe7-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcfe7-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcfe7-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="dcfe7-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcfe7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcfe7-107">DESCRIPTION</span></span>
<span data-ttu-id="dcfe7-108">Командлет **Set-AzDtlVMsPerUserPolicy** задает максимальное количество виртуальных машин, разрешенных для одного пользователя, в пользовательском параметрах лаборатории для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="dcfe7-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="dcfe7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcfe7-110">EXAMPLES</span></span>

## <span data-ttu-id="dcfe7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcfe7-111">PARAMETERS</span></span>

### <span data-ttu-id="dcfe7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfe7-112">-DefaultProfile</span></span>
<span data-ttu-id="dcfe7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dcfe7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcfe7-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="dcfe7-114">-Disable</span></span>
<span data-ttu-id="dcfe7-115">Указывает на то, что этот командлет отключает политику для лаборатории.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="dcfe7-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="dcfe7-116">-Enable</span></span>
<span data-ttu-id="dcfe7-117">Указывает на то, что этот командлет включает политику для лаборатории.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="dcfe7-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="dcfe7-118">-LabName</span></span>
<span data-ttu-id="dcfe7-119">Указывает имя лаборатории, для которой этот командлет задает политику виртуальных машин на пользователя.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="dcfe7-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="dcfe7-120">-MaxVMs</span></span>
<span data-ttu-id="dcfe7-121">Указывает максимальное количество виртуальных машин, которые можно создать в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcfe7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcfe7-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcfe7-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="dcfe7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcfe7-124">-Confirm</span></span>
<span data-ttu-id="dcfe7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcfe7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcfe7-126">-WhatIf</span></span>
<span data-ttu-id="dcfe7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcfe7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcfe7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfe7-129">CommonParameters</span></span>
<span data-ttu-id="dcfe7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcfe7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfe7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcfe7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfe7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcfe7-132">INPUTS</span></span>

### <span data-ttu-id="dcfe7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dcfe7-133">System.String</span></span>

## <span data-ttu-id="dcfe7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcfe7-134">OUTPUTS</span></span>

### <span data-ttu-id="dcfe7-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="dcfe7-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="dcfe7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcfe7-136">NOTES</span></span>

## <span data-ttu-id="dcfe7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcfe7-137">RELATED LINKS</span></span>

[<span data-ttu-id="dcfe7-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="dcfe7-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


