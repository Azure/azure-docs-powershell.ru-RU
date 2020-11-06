---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 48922d3e0cbf8cf322d25657c76ee01e0ee238b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558583"
---
# <span data-ttu-id="4ffd5-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4ffd5-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="4ffd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ffd5-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffd5-103">Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="4ffd5-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ffd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ffd5-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ffd5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffd5-105">DESCRIPTION</span></span>
<span data-ttu-id="4ffd5-106">Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="4ffd5-106">Create a new application insights resource</span></span>

## <span data-ttu-id="4ffd5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffd5-107">EXAMPLES</span></span>

### <span data-ttu-id="4ffd5-108">Пример 1. Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="4ffd5-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
```

<span data-ttu-id="4ffd5-109">Добавьте новый ресурс Application Insights под названием "тест" в группе ресурсов "testgroup" с помощью типа "Java".</span><span class="sxs-lookup"><span data-stu-id="4ffd5-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="4ffd5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ffd5-110">PARAMETERS</span></span>

### <span data-ttu-id="4ffd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffd5-111">-DefaultProfile</span></span>
<span data-ttu-id="4ffd5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ffd5-113">-Видах</span><span class="sxs-lookup"><span data-stu-id="4ffd5-113">-Kind</span></span>
<span data-ttu-id="4ffd5-114">Виды приложения.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4ffd5-115">-Location</span></span>
<span data-ttu-id="4ffd5-116">Расположение ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-116">Application Insights Resource Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ffd5-117">-Name</span></span>
<span data-ttu-id="4ffd5-118">Название ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffd5-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ffd5-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="4ffd5-121">-Tag</span></span>
<span data-ttu-id="4ffd5-122">Теги компонентов.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-122">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ffd5-123">-Confirm</span></span>
<span data-ttu-id="4ffd5-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffd5-125">-WhatIf</span></span>
<span data-ttu-id="4ffd5-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ffd5-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ffd5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffd5-128">CommonParameters</span></span>
<span data-ttu-id="4ffd5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ffd5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffd5-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffd5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffd5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ffd5-131">INPUTS</span></span>

### <span data-ttu-id="4ffd5-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="4ffd5-132">None</span></span>

## <span data-ttu-id="4ffd5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffd5-133">OUTPUTS</span></span>

### <span data-ttu-id="4ffd5-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="4ffd5-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="4ffd5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ffd5-135">NOTES</span></span>

## <span data-ttu-id="4ffd5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ffd5-136">RELATED LINKS</span></span>
