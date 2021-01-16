---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407351"
---
# <span data-ttu-id="d18ae-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="d18ae-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="d18ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d18ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d18ae-103">Получить конфигурации обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="d18ae-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="d18ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d18ae-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d18ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d18ae-105">DESCRIPTION</span></span>
<span data-ttu-id="d18ae-106">Для этого с помощью cmdlet **Get-AzFrontDoorRulesEngine** требуется определенная конфигурация обн.правил или все конфигурации ярлыка правил, связанные с передней линией.</span><span class="sxs-lookup"><span data-stu-id="d18ae-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="d18ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d18ae-107">EXAMPLES</span></span>

### <span data-ttu-id="d18ae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d18ae-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="d18ae-109">Получите определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="d18ae-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="d18ae-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d18ae-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="d18ae-111">Настройка всех конфигураций обдвижки правил на переднем окнах.</span><span class="sxs-lookup"><span data-stu-id="d18ae-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="d18ae-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d18ae-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="d18ae-113">Ожидаемый выход при получении несущества обвода правил.</span><span class="sxs-lookup"><span data-stu-id="d18ae-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="d18ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d18ae-114">PARAMETERS</span></span>

### <span data-ttu-id="d18ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d18ae-115">-DefaultProfile</span></span>
<span data-ttu-id="d18ae-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d18ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d18ae-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d18ae-117">-FrontDoorName</span></span>
<span data-ttu-id="d18ae-118">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="d18ae-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18ae-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d18ae-119">-Name</span></span>
<span data-ttu-id="d18ae-120">Имя обл. правил.</span><span class="sxs-lookup"><span data-stu-id="d18ae-120">Rules engine name.</span></span>

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

### <span data-ttu-id="d18ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d18ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="d18ae-122">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="d18ae-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d18ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d18ae-123">CommonParameters</span></span>
<span data-ttu-id="d18ae-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d18ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d18ae-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d18ae-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d18ae-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d18ae-126">INPUTS</span></span>

### <span data-ttu-id="d18ae-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d18ae-127">None</span></span>

## <span data-ttu-id="d18ae-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d18ae-128">OUTPUTS</span></span>

### <span data-ttu-id="d18ae-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="d18ae-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="d18ae-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d18ae-130">NOTES</span></span>

## <span data-ttu-id="d18ae-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d18ae-131">RELATED LINKS</span></span>
