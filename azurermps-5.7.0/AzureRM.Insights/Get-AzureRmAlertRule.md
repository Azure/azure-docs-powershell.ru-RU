---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557336"
---
# <span data-ttu-id="0fc75-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc75-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="0fc75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fc75-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc75-103">Возвращает правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="0fc75-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fc75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fc75-104">SYNTAX</span></span>

### <span data-ttu-id="0fc75-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0fc75-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fc75-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="0fc75-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fc75-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="0fc75-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fc75-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc75-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc75-109">Командлет **Get-AzureRmAlertRule** получает правило оповещения по имени или URI-адресу или ко всем правилам оповещений из определенной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fc75-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="0fc75-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fc75-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc75-111">Пример 1: получение правил оповещения для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0fc75-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="0fc75-112">Эта команда получает все правила оповещения для группы ресурсов по умолчанию — Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="0fc75-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="0fc75-113">Выходные данные не содержат сведений о правилах, так как параметр *DetailedOutput* не указан.</span><span class="sxs-lookup"><span data-stu-id="0fc75-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="0fc75-114">Пример 2: получение правила оповещения по имени</span><span class="sxs-lookup"><span data-stu-id="0fc75-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="0fc75-115">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="0fc75-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="0fc75-116">Так как параметр *DetailedOutput* не указан, в выходных данных содержатся только основные сведения о правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="0fc75-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="0fc75-117">Пример 3: получение правила оповещения по имени с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="0fc75-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="0fc75-118">Эта команда возвращает правило оповещения с именем myAlert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="0fc75-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="0fc75-119">Указан параметр *DetailedOutput* , поэтому выходные данные подробно описаны.</span><span class="sxs-lookup"><span data-stu-id="0fc75-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="0fc75-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fc75-120">PARAMETERS</span></span>

### <span data-ttu-id="0fc75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc75-121">-DefaultProfile</span></span>
<span data-ttu-id="0fc75-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0fc75-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fc75-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="0fc75-123">-DetailedOutput</span></span>
<span data-ttu-id="0fc75-124">Отображение подробных сведений в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0fc75-124">Displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc75-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fc75-125">-Name</span></span>
<span data-ttu-id="0fc75-126">Указывает имя правила оповещения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="0fc75-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc75-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc75-127">-ResourceGroupName</span></span>
<span data-ttu-id="0fc75-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fc75-128">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc75-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0fc75-129">-TargetResourceId</span></span>
<span data-ttu-id="0fc75-130">Указывает идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="0fc75-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc75-131">CommonParameters</span></span>
<span data-ttu-id="0fc75-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fc75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc75-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc75-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc75-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fc75-134">INPUTS</span></span>

### <span data-ttu-id="0fc75-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="0fc75-135">None</span></span>
<span data-ttu-id="0fc75-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0fc75-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fc75-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fc75-137">OUTPUTS</span></span>

### <span data-ttu-id="0fc75-138">List<Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule></span><span class="sxs-lookup"><span data-stu-id="0fc75-138">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule></span></span>

## <span data-ttu-id="0fc75-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fc75-139">NOTES</span></span>

## <span data-ttu-id="0fc75-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fc75-140">RELATED LINKS</span></span>

[<span data-ttu-id="0fc75-141">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc75-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="0fc75-142">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc75-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="0fc75-143">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc75-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="0fc75-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="0fc75-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="0fc75-145">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="0fc75-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


