---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 62ef80d7af7ce9b9a10a7a18b38fbf5c6f1db562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994258"
---
# <span data-ttu-id="5db90-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="5db90-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="5db90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db90-102">SYNOPSIS</span></span>
<span data-ttu-id="5db90-103">Получить конфигурации обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="5db90-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="5db90-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5db90-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db90-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5db90-105">DESCRIPTION</span></span>
<span data-ttu-id="5db90-106">Для этого с помощью cmdlet **Get-AzFrontDoorRulesEngine** требуется определенная конфигурация обн.правил или все конфигурации ярлыка правил, связанные с передней линией.</span><span class="sxs-lookup"><span data-stu-id="5db90-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="5db90-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5db90-107">EXAMPLES</span></span>

### <span data-ttu-id="5db90-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5db90-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="5db90-109">Получите определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="5db90-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="5db90-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5db90-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="5db90-111">Настройка всех конфигураций обдвижки правил на переднем окнах.</span><span class="sxs-lookup"><span data-stu-id="5db90-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="5db90-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5db90-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="5db90-113">Ожидаемый выход при получении несущества обвода правил.</span><span class="sxs-lookup"><span data-stu-id="5db90-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="5db90-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5db90-114">PARAMETERS</span></span>

### <span data-ttu-id="5db90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db90-115">-DefaultProfile</span></span>
<span data-ttu-id="5db90-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5db90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db90-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="5db90-117">-FrontDoorName</span></span>
<span data-ttu-id="5db90-118">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="5db90-118">Front Door name.</span></span>

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

### <span data-ttu-id="5db90-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5db90-119">-Name</span></span>
<span data-ttu-id="5db90-120">Имя яла правила.</span><span class="sxs-lookup"><span data-stu-id="5db90-120">Rules engine name.</span></span>

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

### <span data-ttu-id="5db90-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db90-121">-ResourceGroupName</span></span>
<span data-ttu-id="5db90-122">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="5db90-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="5db90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db90-123">CommonParameters</span></span>
<span data-ttu-id="5db90-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db90-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5db90-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db90-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5db90-126">INPUTS</span></span>

### <span data-ttu-id="5db90-127">Нет</span><span class="sxs-lookup"><span data-stu-id="5db90-127">None</span></span>

## <span data-ttu-id="5db90-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5db90-128">OUTPUTS</span></span>

### <span data-ttu-id="5db90-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="5db90-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="5db90-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5db90-130">NOTES</span></span>

## <span data-ttu-id="5db90-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5db90-131">RELATED LINKS</span></span>
