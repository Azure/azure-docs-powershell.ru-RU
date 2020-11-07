---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: a1efa9159bbe318a1de0360a3f70f197660db535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733735"
---
# <span data-ttu-id="05f70-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="05f70-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="05f70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05f70-102">SYNOPSIS</span></span>
<span data-ttu-id="05f70-103">Задает политику автоматического запуска лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="05f70-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05f70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05f70-104">SYNTAX</span></span>

### <span data-ttu-id="05f70-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05f70-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05f70-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="05f70-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05f70-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05f70-107">DESCRIPTION</span></span>
<span data-ttu-id="05f70-108">Командлет **Set-AzureRmDtlAutoStartPolicy** задает политику автоматического запуска лаборатории, позволяющую планировать автоматическое начало для виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="05f70-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="05f70-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05f70-110">EXAMPLES</span></span>

## <span data-ttu-id="05f70-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05f70-111">PARAMETERS</span></span>

### <span data-ttu-id="05f70-112">-Days</span><span class="sxs-lookup"><span data-stu-id="05f70-112">-Days</span></span>
<span data-ttu-id="05f70-113">Указывает в виде массива дни недели, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="05f70-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="05f70-114">-Disable</span></span>
<span data-ttu-id="05f70-115">Указывает, что этот командлет отключает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-115">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="05f70-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="05f70-116">-Enable</span></span>
<span data-ttu-id="05f70-117">Указывает на то, что этот командлет включает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-117">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="05f70-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="05f70-118">-LabName</span></span>
<span data-ttu-id="05f70-119">Указывает имя лаборатории, для которой этот командлет задает политику автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="05f70-119">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="05f70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f70-120">-ResourceGroupName</span></span>
<span data-ttu-id="05f70-121">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="05f70-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="05f70-122">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="05f70-122">-Time</span></span>
<span data-ttu-id="05f70-123">Указывает время, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-123">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="05f70-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05f70-124">-Confirm</span></span>
<span data-ttu-id="05f70-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05f70-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05f70-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05f70-126">-WhatIf</span></span>
<span data-ttu-id="05f70-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05f70-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05f70-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05f70-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05f70-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f70-129">-DefaultProfile</span></span>
<span data-ttu-id="05f70-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05f70-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05f70-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f70-131">CommonParameters</span></span>
<span data-ttu-id="05f70-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05f70-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f70-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05f70-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f70-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05f70-134">INPUTS</span></span>

## <span data-ttu-id="05f70-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05f70-135">OUTPUTS</span></span>

### <span data-ttu-id="05f70-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="05f70-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="05f70-137">Этот командлет возвращает расписание, которое определяет, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="05f70-137">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="05f70-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="05f70-138">NOTES</span></span>

## <span data-ttu-id="05f70-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05f70-139">RELATED LINKS</span></span>

[<span data-ttu-id="05f70-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="05f70-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


