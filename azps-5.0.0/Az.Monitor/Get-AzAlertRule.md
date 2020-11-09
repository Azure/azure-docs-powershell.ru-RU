---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248604"
---
# <span data-ttu-id="89066-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="89066-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="89066-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89066-102">SYNOPSIS</span></span>
<span data-ttu-id="89066-103">Возвращает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="89066-103">Gets alert rules.</span></span>

## <span data-ttu-id="89066-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89066-104">SYNTAX</span></span>

### <span data-ttu-id="89066-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89066-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89066-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="89066-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89066-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="89066-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89066-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89066-108">DESCRIPTION</span></span>
<span data-ttu-id="89066-109">Командлет **Get-AzAlertRule** получает правило оповещения по имени или URI-адресу или ко всем правилам оповещений из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89066-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="89066-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89066-110">EXAMPLES</span></span>

### <span data-ttu-id="89066-111">Пример 1: получение правил оповещения для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="89066-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="89066-112">Эта команда получает все правила оповещения для группы ресурсов по умолчанию — Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="89066-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="89066-113">Выходные данные не содержат сведений о правилах, так как параметр *DetailedOutput* не указан.</span><span class="sxs-lookup"><span data-stu-id="89066-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="89066-114">Пример 2: получение правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="89066-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="89066-115">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="89066-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="89066-116">Так как параметр *DetailedOutput* не указан, в выходных данных содержатся только основные сведения о правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="89066-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="89066-117">Пример 3: получение правила оповещения по имени с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="89066-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="89066-118">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="89066-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="89066-119">Указан параметр *DetailedOutput* , поэтому выходные данные подробно описаны.</span><span class="sxs-lookup"><span data-stu-id="89066-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="89066-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89066-120">PARAMETERS</span></span>

### <span data-ttu-id="89066-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89066-121">-DefaultProfile</span></span>
<span data-ttu-id="89066-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89066-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89066-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="89066-123">-DetailedOutput</span></span>
<span data-ttu-id="89066-124">Отображение подробных сведений в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="89066-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="89066-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89066-125">-Name</span></span>
<span data-ttu-id="89066-126">Указывает имя правила оповещения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="89066-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="89066-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89066-127">-ResourceGroupName</span></span>
<span data-ttu-id="89066-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89066-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="89066-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="89066-129">-TargetResourceId</span></span>
<span data-ttu-id="89066-130">Указывает идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="89066-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="89066-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89066-131">CommonParameters</span></span>
<span data-ttu-id="89066-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89066-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89066-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89066-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89066-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89066-134">INPUTS</span></span>

### <span data-ttu-id="89066-135">System. String</span><span class="sxs-lookup"><span data-stu-id="89066-135">System.String</span></span>

### <span data-ttu-id="89066-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89066-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89066-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89066-137">OUTPUTS</span></span>

### <span data-ttu-id="89066-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="89066-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="89066-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="89066-139">NOTES</span></span>

## <span data-ttu-id="89066-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89066-140">RELATED LINKS</span></span>

[<span data-ttu-id="89066-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="89066-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="89066-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="89066-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="89066-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="89066-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="89066-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="89066-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="89066-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="89066-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)

