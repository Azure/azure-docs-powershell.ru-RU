---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 98232807cc5f7624242cd44c7d27579ef0f92d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958696"
---
# <span data-ttu-id="c99b8-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c99b8-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="c99b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c99b8-103">Получает приложение логики из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c99b8-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="c99b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c99b8-104">SYNTAX</span></span>

### <span data-ttu-id="c99b8-105">ListWorkflows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c99b8-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c99b8-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="c99b8-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99b8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99b8-107">DESCRIPTION</span></span>
<span data-ttu-id="c99b8-108">Для **работы с помощью cmdlet Get-AzLogicApp** можно выбрать приложение логики.</span><span class="sxs-lookup"><span data-stu-id="c99b8-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="c99b8-109">Этот cmdlet возвращает объект **рабочего** процесса.</span><span class="sxs-lookup"><span data-stu-id="c99b8-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="c99b8-110">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="c99b8-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c99b8-111">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="c99b8-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c99b8-112">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="c99b8-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c99b8-113">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="c99b8-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c99b8-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c99b8-114">EXAMPLES</span></span>

### <span data-ttu-id="c99b8-115">Пример 1. Получить приложение логики из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c99b8-115">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="c99b8-116">Эта команда получает приложение логики из группы ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c99b8-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="c99b8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c99b8-117">PARAMETERS</span></span>

### <span data-ttu-id="c99b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99b8-118">-DefaultProfile</span></span>
<span data-ttu-id="c99b8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c99b8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c99b8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c99b8-120">-Name</span></span>
<span data-ttu-id="c99b8-121">Указывает имя приложения логики, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c99b8-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c99b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="c99b8-123">Имя группы ресурсов, в которой этот cmdlet получает приложение логики.</span><span class="sxs-lookup"><span data-stu-id="c99b8-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="c99b8-124">-Версия</span><span class="sxs-lookup"><span data-stu-id="c99b8-124">-Version</span></span>
<span data-ttu-id="c99b8-125">Указывает версию приложения логики.</span><span class="sxs-lookup"><span data-stu-id="c99b8-125">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="c99b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99b8-126">CommonParameters</span></span>
<span data-ttu-id="c99b8-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99b8-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99b8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99b8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c99b8-129">INPUTS</span></span>

### <span data-ttu-id="c99b8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c99b8-130">System.String</span></span>

## <span data-ttu-id="c99b8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c99b8-131">OUTPUTS</span></span>

### <span data-ttu-id="c99b8-132">Microsoft.Azure.Management.Logic.Models.Workflow</span><span class="sxs-lookup"><span data-stu-id="c99b8-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="c99b8-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="c99b8-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="c99b8-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c99b8-134">NOTES</span></span>

## <span data-ttu-id="c99b8-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c99b8-135">RELATED LINKS</span></span>

[<span data-ttu-id="c99b8-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c99b8-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="c99b8-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c99b8-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="c99b8-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c99b8-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="c99b8-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c99b8-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


