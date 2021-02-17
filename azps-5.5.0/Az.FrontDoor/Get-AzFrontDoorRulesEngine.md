---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243584"
---
# <span data-ttu-id="523b1-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="523b1-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="523b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="523b1-102">SYNOPSIS</span></span>
<span data-ttu-id="523b1-103">Получить конфигурации обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="523b1-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="523b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="523b1-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="523b1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="523b1-105">DESCRIPTION</span></span>
<span data-ttu-id="523b1-106">Для этого с помощью cmdlet **Get-AzFrontDoorRulesEngine** требуется определенная конфигурация обн.</span><span class="sxs-lookup"><span data-stu-id="523b1-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="523b1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="523b1-107">EXAMPLES</span></span>

### <span data-ttu-id="523b1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="523b1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="523b1-109">Получите определенную конфигурацию обдвижки правил.</span><span class="sxs-lookup"><span data-stu-id="523b1-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="523b1-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="523b1-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="523b1-111">Настройка всех конфигураций обдвижки правил на переднем окнах.</span><span class="sxs-lookup"><span data-stu-id="523b1-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="523b1-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="523b1-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="523b1-113">Ожидаемый выход при получении несущества обвода правил.</span><span class="sxs-lookup"><span data-stu-id="523b1-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="523b1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="523b1-114">PARAMETERS</span></span>

### <span data-ttu-id="523b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523b1-115">-DefaultProfile</span></span>
<span data-ttu-id="523b1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="523b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="523b1-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="523b1-117">-FrontDoorName</span></span>
<span data-ttu-id="523b1-118">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="523b1-118">Front Door name.</span></span>

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

### <span data-ttu-id="523b1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="523b1-119">-Name</span></span>
<span data-ttu-id="523b1-120">Имя обл. правил.</span><span class="sxs-lookup"><span data-stu-id="523b1-120">Rules engine name.</span></span>

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

### <span data-ttu-id="523b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="523b1-122">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="523b1-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="523b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523b1-123">CommonParameters</span></span>
<span data-ttu-id="523b1-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523b1-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="523b1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523b1-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="523b1-126">INPUTS</span></span>

### <span data-ttu-id="523b1-127">Нет</span><span class="sxs-lookup"><span data-stu-id="523b1-127">None</span></span>

## <span data-ttu-id="523b1-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="523b1-128">OUTPUTS</span></span>

### <span data-ttu-id="523b1-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="523b1-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="523b1-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="523b1-130">NOTES</span></span>

## <span data-ttu-id="523b1-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="523b1-131">RELATED LINKS</span></span>
