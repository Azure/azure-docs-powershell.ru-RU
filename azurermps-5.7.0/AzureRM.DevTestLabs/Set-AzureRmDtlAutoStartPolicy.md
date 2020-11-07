---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 000c9f2748bd1f80559d9fc80c206e4f1c9bf0c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733284"
---
# <span data-ttu-id="c72d9-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="c72d9-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="c72d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c72d9-102">SYNOPSIS</span></span>
<span data-ttu-id="c72d9-103">Задает политику автоматического запуска лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="c72d9-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c72d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c72d9-104">SYNTAX</span></span>

### <span data-ttu-id="c72d9-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c72d9-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c72d9-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="c72d9-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c72d9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c72d9-107">DESCRIPTION</span></span>
<span data-ttu-id="c72d9-108">Командлет **Set-AzureRmDtlAutoStartPolicy** задает политику автоматического запуска лаборатории, позволяющую планировать автоматическое начало для виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="c72d9-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="c72d9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c72d9-110">EXAMPLES</span></span>

## <span data-ttu-id="c72d9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c72d9-111">PARAMETERS</span></span>

### <span data-ttu-id="c72d9-112">-Days</span><span class="sxs-lookup"><span data-stu-id="c72d9-112">-Days</span></span>
<span data-ttu-id="c72d9-113">Указывает в виде массива дни недели, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72d9-114">-DefaultProfile</span></span>
<span data-ttu-id="c72d9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c72d9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c72d9-116">-Отключение</span><span class="sxs-lookup"><span data-stu-id="c72d9-116">-Disable</span></span>
<span data-ttu-id="c72d9-117">Указывает, что этот командлет отключает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="c72d9-118">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="c72d9-118">-Enable</span></span>
<span data-ttu-id="c72d9-119">Указывает на то, что этот командлет включает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="c72d9-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="c72d9-120">-LabName</span></span>
<span data-ttu-id="c72d9-121">Указывает имя лаборатории, для которой этот командлет задает политику автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="c72d9-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="c72d9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c72d9-122">-ResourceGroupName</span></span>
<span data-ttu-id="c72d9-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="c72d9-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c72d9-124">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="c72d9-124">-Time</span></span>
<span data-ttu-id="c72d9-125">Указывает время, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c72d9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c72d9-126">-Confirm</span></span>
<span data-ttu-id="c72d9-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c72d9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72d9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c72d9-128">-WhatIf</span></span>
<span data-ttu-id="c72d9-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c72d9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c72d9-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c72d9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72d9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72d9-131">CommonParameters</span></span>
<span data-ttu-id="c72d9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c72d9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72d9-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72d9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72d9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c72d9-134">INPUTS</span></span>

### <span data-ttu-id="c72d9-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="c72d9-135">None</span></span>
<span data-ttu-id="c72d9-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c72d9-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c72d9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c72d9-137">OUTPUTS</span></span>

### <span data-ttu-id="c72d9-138">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="c72d9-138">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="c72d9-139">Этот командлет возвращает расписание, которое определяет, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="c72d9-139">This cmdlet returns the schedule that specifies when the virtual machines of the lab must be started.</span></span>

## <span data-ttu-id="c72d9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c72d9-140">NOTES</span></span>

## <span data-ttu-id="c72d9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c72d9-141">RELATED LINKS</span></span>

[<span data-ttu-id="c72d9-142">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="c72d9-142">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


