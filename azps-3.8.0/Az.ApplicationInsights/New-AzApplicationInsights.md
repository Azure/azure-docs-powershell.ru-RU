---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 550fb398dbd636ba9c43c66d31b78384610cf42b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074147"
---
# <span data-ttu-id="ea5c8-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ea5c8-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="ea5c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5c8-103">Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ea5c8-103">Create a new application insights resource</span></span>

## <span data-ttu-id="ea5c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea5c8-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5c8-106">Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ea5c8-106">Create a new application insights resource</span></span>

## <span data-ttu-id="ea5c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="ea5c8-108">Пример 1. Создание нового ресурса Application Insights</span><span class="sxs-lookup"><span data-stu-id="ea5c8-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
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

<span data-ttu-id="ea5c8-109">Добавьте новый ресурс Application Insights под названием "тест" в группе ресурсов "testgroup" с помощью типа "Java".</span><span class="sxs-lookup"><span data-stu-id="ea5c8-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="ea5c8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea5c8-110">PARAMETERS</span></span>

### <span data-ttu-id="ea5c8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5c8-111">-DefaultProfile</span></span>
<span data-ttu-id="ea5c8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea5c8-113">-Видах</span><span class="sxs-lookup"><span data-stu-id="ea5c8-113">-Kind</span></span>
<span data-ttu-id="ea5c8-114">Виды приложения.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-114">Application kind.</span></span>

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

### <span data-ttu-id="ea5c8-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ea5c8-115">-Location</span></span>
<span data-ttu-id="ea5c8-116">Расположение ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="ea5c8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea5c8-117">-Name</span></span>
<span data-ttu-id="ea5c8-118">Название ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="ea5c8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5c8-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea5c8-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea5c8-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="ea5c8-121">-Tag</span></span>
<span data-ttu-id="ea5c8-122">Теги компонентов.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-122">Component Tags.</span></span>

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

### <span data-ttu-id="ea5c8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea5c8-123">-Confirm</span></span>
<span data-ttu-id="ea5c8-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5c8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5c8-125">-WhatIf</span></span>
<span data-ttu-id="ea5c8-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea5c8-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5c8-128">CommonParameters</span></span>
<span data-ttu-id="ea5c8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea5c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5c8-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea5c8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5c8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea5c8-131">INPUTS</span></span>

### <span data-ttu-id="ea5c8-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea5c8-132">None</span></span>

## <span data-ttu-id="ea5c8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea5c8-133">OUTPUTS</span></span>

### <span data-ttu-id="ea5c8-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ea5c8-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="ea5c8-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea5c8-135">NOTES</span></span>

## <span data-ttu-id="ea5c8-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea5c8-136">RELATED LINKS</span></span>
