---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 891f7fcd50281f5dab9b8d4eaf9f1bd842fbc85e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559723"
---
# <span data-ttu-id="603f6-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="603f6-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="603f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="603f6-102">SYNOPSIS</span></span>
<span data-ttu-id="603f6-103">Возвращает логическое приложение из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="603f6-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="603f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="603f6-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="603f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="603f6-105">DESCRIPTION</span></span>
<span data-ttu-id="603f6-106">Командлет **Get-AzureRmLogicApp** получает логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="603f6-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="603f6-107">Этот командлет возвращает объект **рабочего процесса** .</span><span class="sxs-lookup"><span data-stu-id="603f6-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="603f6-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="603f6-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="603f6-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="603f6-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="603f6-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="603f6-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="603f6-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="603f6-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="603f6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="603f6-112">EXAMPLES</span></span>

### <span data-ttu-id="603f6-113">Пример 1: получение логики приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="603f6-113">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="603f6-114">Эта команда возвращает логическое приложение из группы ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="603f6-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="603f6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="603f6-115">PARAMETERS</span></span>

### <span data-ttu-id="603f6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="603f6-116">-Name</span></span>
<span data-ttu-id="603f6-117">Указывает имя приложения логики, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="603f6-117">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="603f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="603f6-119">Указывает имя группы ресурсов, в которой этот командлет получает логическое приложение.</span><span class="sxs-lookup"><span data-stu-id="603f6-119">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="603f6-120">-Version</span><span class="sxs-lookup"><span data-stu-id="603f6-120">-Version</span></span>
<span data-ttu-id="603f6-121">Определяет версию логики приложения.</span><span class="sxs-lookup"><span data-stu-id="603f6-121">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="603f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603f6-122">-DefaultProfile</span></span>
<span data-ttu-id="603f6-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="603f6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="603f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603f6-124">CommonParameters</span></span>
<span data-ttu-id="603f6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="603f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603f6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="603f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603f6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="603f6-127">INPUTS</span></span>

## <span data-ttu-id="603f6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="603f6-128">OUTPUTS</span></span>

### <span data-ttu-id="603f6-129">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="603f6-129">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="603f6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="603f6-130">NOTES</span></span>

## <span data-ttu-id="603f6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="603f6-131">RELATED LINKS</span></span>

[<span data-ttu-id="603f6-132">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="603f6-132">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="603f6-133">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="603f6-133">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="603f6-134">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="603f6-134">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="603f6-135">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="603f6-135">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


