---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 9e1a0035a9736ac01963d150f06db9e510e51e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720329"
---
# <span data-ttu-id="2a7fe-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="2a7fe-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="2a7fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7fe-103">Возвращает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-103">Gets alert rules.</span></span>

## <span data-ttu-id="2a7fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a7fe-104">SYNTAX</span></span>

### <span data-ttu-id="2a7fe-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a7fe-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a7fe-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="2a7fe-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a7fe-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="2a7fe-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a7fe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a7fe-108">DESCRIPTION</span></span>
<span data-ttu-id="2a7fe-109">Командлет **Get-AzAlertRule** получает правило оповещения по имени или URI-адресу или ко всем правилам оповещений из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="2a7fe-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a7fe-110">EXAMPLES</span></span>

### <span data-ttu-id="2a7fe-111">Пример 1: получение правил оповещения для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a7fe-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="2a7fe-112">Эта команда получает все правила оповещения для группы ресурсов по умолчанию — Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="2a7fe-113">Выходные данные не содержат сведений о правилах, так как параметр *DetailedOutput* не указан.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="2a7fe-114">Пример 2: получение правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="2a7fe-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="2a7fe-115">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="2a7fe-116">Так как параметр *DetailedOutput* не указан, в выходных данных содержатся только основные сведения о правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="2a7fe-117">Пример 3: получение правила оповещения по имени с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="2a7fe-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="2a7fe-118">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="2a7fe-119">Указан параметр *DetailedOutput* , поэтому выходные данные подробно описаны.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="2a7fe-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a7fe-120">PARAMETERS</span></span>

### <span data-ttu-id="2a7fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7fe-121">-DefaultProfile</span></span>
<span data-ttu-id="2a7fe-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2a7fe-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a7fe-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="2a7fe-123">-DetailedOutput</span></span>
<span data-ttu-id="2a7fe-124">Отображение подробных сведений в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7fe-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a7fe-125">-Name</span></span>
<span data-ttu-id="2a7fe-126">Указывает имя правила оповещения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a7fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a7fe-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7fe-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2a7fe-129">-TargetResourceId</span></span>
<span data-ttu-id="2a7fe-130">Указывает идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7fe-131">CommonParameters</span></span>
<span data-ttu-id="2a7fe-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a7fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7fe-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a7fe-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7fe-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a7fe-134">INPUTS</span></span>

### <span data-ttu-id="2a7fe-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2a7fe-135">System.String</span></span>

### <span data-ttu-id="2a7fe-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a7fe-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a7fe-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a7fe-137">OUTPUTS</span></span>

### <span data-ttu-id="2a7fe-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="2a7fe-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="2a7fe-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a7fe-139">NOTES</span></span>

## <span data-ttu-id="2a7fe-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a7fe-140">RELATED LINKS</span></span>

[<span data-ttu-id="2a7fe-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="2a7fe-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="2a7fe-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2a7fe-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="2a7fe-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2a7fe-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="2a7fe-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2a7fe-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="2a7fe-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="2a7fe-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


