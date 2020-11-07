---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912210"
---
# <span data-ttu-id="fc82a-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fc82a-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="fc82a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc82a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc82a-103">Возвращает логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc82a-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="fc82a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc82a-104">SYNTAX</span></span>

### <span data-ttu-id="fc82a-105">ListWorkflows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc82a-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc82a-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="fc82a-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc82a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc82a-107">DESCRIPTION</span></span>
<span data-ttu-id="fc82a-108">Командлет **Get-AzLogicApp** получает логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="fc82a-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="fc82a-109">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="fc82a-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="fc82a-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="fc82a-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="fc82a-111">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="fc82a-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="fc82a-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="fc82a-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="fc82a-113">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="fc82a-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="fc82a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc82a-114">EXAMPLES</span></span>

### <span data-ttu-id="fc82a-115">Пример 1: получение логики приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fc82a-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="fc82a-116">Эта команда возвращает логическое приложение из группы ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fc82a-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="fc82a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc82a-117">PARAMETERS</span></span>

### <span data-ttu-id="fc82a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc82a-118">-DefaultProfile</span></span>
<span data-ttu-id="fc82a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fc82a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc82a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc82a-120">-Name</span></span>
<span data-ttu-id="fc82a-121">Указывает имя приложения логики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fc82a-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc82a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc82a-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc82a-123">Указывает имя группы ресурсов, в которой этот командлет получает логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="fc82a-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc82a-124">-Version</span><span class="sxs-lookup"><span data-stu-id="fc82a-124">-Version</span></span>
<span data-ttu-id="fc82a-125">Определяет версию логики приложения.</span><span class="sxs-lookup"><span data-stu-id="fc82a-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc82a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc82a-126">CommonParameters</span></span>
<span data-ttu-id="fc82a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc82a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc82a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc82a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc82a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc82a-129">INPUTS</span></span>

### <span data-ttu-id="fc82a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fc82a-130">System.String</span></span>

## <span data-ttu-id="fc82a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc82a-131">OUTPUTS</span></span>

### <span data-ttu-id="fc82a-132">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="fc82a-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="fc82a-133">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="fc82a-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="fc82a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc82a-134">NOTES</span></span>

## <span data-ttu-id="fc82a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc82a-135">RELATED LINKS</span></span>

[<span data-ttu-id="fc82a-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fc82a-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="fc82a-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fc82a-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="fc82a-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fc82a-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="fc82a-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="fc82a-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


