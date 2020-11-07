---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4b15f20f9399df277fc2d2a76f7e51c2a7d57d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730944"
---
# <span data-ttu-id="fee7a-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="fee7a-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="fee7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fee7a-102">SYNOPSIS</span></span>
<span data-ttu-id="fee7a-103">Задает политику автоматического выключения лабораторных семинаров DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="fee7a-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="fee7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fee7a-104">SYNTAX</span></span>

### <span data-ttu-id="fee7a-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fee7a-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee7a-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="fee7a-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee7a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee7a-107">DESCRIPTION</span></span>
<span data-ttu-id="fee7a-108">Командлет **Set-AzDtlAutoShutdownPolicy** задает политику автоматического отключения лаборатории, которая автоматически завершает работу всех виртуальных машин в лаборатории в заданное время суток.</span><span class="sxs-lookup"><span data-stu-id="fee7a-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="fee7a-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="fee7a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="fee7a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fee7a-110">EXAMPLES</span></span>

## <span data-ttu-id="fee7a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fee7a-111">PARAMETERS</span></span>

### <span data-ttu-id="fee7a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee7a-112">-DefaultProfile</span></span>
<span data-ttu-id="fee7a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fee7a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fee7a-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="fee7a-114">-Disable</span></span>
<span data-ttu-id="fee7a-115">Указывает на то, что командлет отключает политику в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="fee7a-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="fee7a-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="fee7a-116">-Enable</span></span>
<span data-ttu-id="fee7a-117">Указывает на то, что командлет включает политику в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="fee7a-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="fee7a-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="fee7a-118">-LabName</span></span>
<span data-ttu-id="fee7a-119">Указывает имя лаборатории, для которой этот командлет задает политику автоматического отключения.</span><span class="sxs-lookup"><span data-stu-id="fee7a-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="fee7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="fee7a-121">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="fee7a-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="fee7a-122">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="fee7a-122">-Time</span></span>
<span data-ttu-id="fee7a-123">Задает время в виде объекта **DateTime** , по истечении которого виртуальные машины в лаборатории должны завершить работу.</span><span class="sxs-lookup"><span data-stu-id="fee7a-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="fee7a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee7a-124">-Confirm</span></span>
<span data-ttu-id="fee7a-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fee7a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee7a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee7a-126">-WhatIf</span></span>
<span data-ttu-id="fee7a-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fee7a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee7a-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fee7a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee7a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee7a-129">CommonParameters</span></span>
<span data-ttu-id="fee7a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fee7a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee7a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee7a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee7a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fee7a-132">INPUTS</span></span>

### <span data-ttu-id="fee7a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fee7a-133">System.String</span></span>

## <span data-ttu-id="fee7a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee7a-134">OUTPUTS</span></span>

### <span data-ttu-id="fee7a-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="fee7a-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="fee7a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="fee7a-136">NOTES</span></span>

## <span data-ttu-id="fee7a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fee7a-137">RELATED LINKS</span></span>

[<span data-ttu-id="fee7a-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="fee7a-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


