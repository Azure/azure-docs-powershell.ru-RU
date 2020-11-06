---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 740ef9b21a2e2caa839880ff2c5e9dadc042351a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568512"
---
# <span data-ttu-id="c79c3-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c79c3-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="c79c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c79c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c79c3-103">Возвращает логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c79c3-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c79c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c79c3-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c79c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c79c3-105">DESCRIPTION</span></span>
<span data-ttu-id="c79c3-106">Командлет **Get-AzureRmLogicApp** получает логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="c79c3-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="c79c3-107">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="c79c3-107">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="c79c3-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="c79c3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c79c3-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="c79c3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c79c3-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="c79c3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c79c3-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="c79c3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c79c3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c79c3-112">EXAMPLES</span></span>

### <span data-ttu-id="c79c3-113">Пример 1: получение логики приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c79c3-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="c79c3-114">Эта команда возвращает логическое приложение из группы ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c79c3-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="c79c3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c79c3-115">PARAMETERS</span></span>

### <span data-ttu-id="c79c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79c3-116">-DefaultProfile</span></span>
<span data-ttu-id="c79c3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c79c3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c79c3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c79c3-118">-Name</span></span>
<span data-ttu-id="c79c3-119">Указывает имя приложения логики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c79c3-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79c3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79c3-120">-ResourceGroupName</span></span>
<span data-ttu-id="c79c3-121">Указывает имя группы ресурсов, в которой этот командлет получает логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="c79c3-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79c3-122">-Version</span><span class="sxs-lookup"><span data-stu-id="c79c3-122">-Version</span></span>
<span data-ttu-id="c79c3-123">Определяет версию логики приложения.</span><span class="sxs-lookup"><span data-stu-id="c79c3-123">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79c3-124">CommonParameters</span></span>
<span data-ttu-id="c79c3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c79c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79c3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79c3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c79c3-127">INPUTS</span></span>

### <span data-ttu-id="c79c3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c79c3-128">System.String</span></span>

## <span data-ttu-id="c79c3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c79c3-129">OUTPUTS</span></span>

### <span data-ttu-id="c79c3-130">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="c79c3-130">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="c79c3-131">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="c79c3-131">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="c79c3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c79c3-132">NOTES</span></span>

## <span data-ttu-id="c79c3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c79c3-133">RELATED LINKS</span></span>

[<span data-ttu-id="c79c3-134">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c79c3-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="c79c3-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c79c3-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="c79c3-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c79c3-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="c79c3-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c79c3-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


