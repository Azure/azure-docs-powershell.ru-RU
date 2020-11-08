---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 7031aaa5a0e5655f933beadbb51569aba0adbef1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066857"
---
# <span data-ttu-id="98d36-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="98d36-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="98d36-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98d36-102">SYNOPSIS</span></span>
<span data-ttu-id="98d36-103">Задает политику автоматического запуска лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="98d36-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="98d36-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98d36-104">SYNTAX</span></span>

### <span data-ttu-id="98d36-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98d36-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98d36-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="98d36-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98d36-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98d36-107">DESCRIPTION</span></span>
<span data-ttu-id="98d36-108">Командлет **Set-AzDtlAutoStartPolicy** задает политику автоматического запуска лаборатории, позволяющую планировать автоматическое начало для виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="98d36-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="98d36-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="98d36-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="98d36-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98d36-110">EXAMPLES</span></span>

## <span data-ttu-id="98d36-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98d36-111">PARAMETERS</span></span>

### <span data-ttu-id="98d36-112">-Days</span><span class="sxs-lookup"><span data-stu-id="98d36-112">-Days</span></span>
<span data-ttu-id="98d36-113">Указывает в виде массива дни недели, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="98d36-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d36-114">-DefaultProfile</span></span>
<span data-ttu-id="98d36-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98d36-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98d36-116">-Отключение</span><span class="sxs-lookup"><span data-stu-id="98d36-116">-Disable</span></span>
<span data-ttu-id="98d36-117">Указывает, что этот командлет отключает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="98d36-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="98d36-118">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="98d36-118">-Enable</span></span>
<span data-ttu-id="98d36-119">Указывает на то, что этот командлет включает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="98d36-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="98d36-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="98d36-120">-LabName</span></span>
<span data-ttu-id="98d36-121">Указывает имя лаборатории, для которой этот командлет задает политику автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="98d36-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="98d36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d36-122">-ResourceGroupName</span></span>
<span data-ttu-id="98d36-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="98d36-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="98d36-124">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="98d36-124">-Time</span></span>
<span data-ttu-id="98d36-125">Указывает время, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="98d36-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98d36-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98d36-126">-Confirm</span></span>
<span data-ttu-id="98d36-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98d36-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d36-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d36-128">-WhatIf</span></span>
<span data-ttu-id="98d36-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98d36-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98d36-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98d36-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d36-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d36-131">CommonParameters</span></span>
<span data-ttu-id="98d36-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98d36-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d36-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d36-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d36-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98d36-134">INPUTS</span></span>

### <span data-ttu-id="98d36-135">System. String</span><span class="sxs-lookup"><span data-stu-id="98d36-135">System.String</span></span>

## <span data-ttu-id="98d36-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98d36-136">OUTPUTS</span></span>

### <span data-ttu-id="98d36-137">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="98d36-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="98d36-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="98d36-138">NOTES</span></span>

## <span data-ttu-id="98d36-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98d36-139">RELATED LINKS</span></span>

[<span data-ttu-id="98d36-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="98d36-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)


