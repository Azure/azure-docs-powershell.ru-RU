---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249057"
---
# <span data-ttu-id="c2b71-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c2b71-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="c2b71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2b71-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b71-103">Получение конфигураций обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="c2b71-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="c2b71-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2b71-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b71-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2b71-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b71-106">Командлет **Get-AzFrontDoorRulesEngine** возвращает определенную конфигурацию обработчика правил или получает все конфигурации обработчика правил, связанные с передней дверцей.</span><span class="sxs-lookup"><span data-stu-id="c2b71-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="c2b71-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2b71-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b71-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2b71-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="c2b71-109">Получить определенную конфигурацию обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="c2b71-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="c2b71-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c2b71-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="c2b71-111">Получение всех конфигураций обработчика правил на передней дверце.</span><span class="sxs-lookup"><span data-stu-id="c2b71-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="c2b71-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c2b71-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="c2b71-113">Ожидаемый вывод при извлечении несуществующего обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="c2b71-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="c2b71-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2b71-114">PARAMETERS</span></span>

### <span data-ttu-id="c2b71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b71-115">-DefaultProfile</span></span>
<span data-ttu-id="c2b71-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b71-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c2b71-117">-FrontDoorName</span></span>
<span data-ttu-id="c2b71-118">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="c2b71-118">Front Door name.</span></span>

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

### <span data-ttu-id="c2b71-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2b71-119">-Name</span></span>
<span data-ttu-id="c2b71-120">Имя обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="c2b71-120">Rules engine name.</span></span>

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

### <span data-ttu-id="c2b71-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b71-121">-ResourceGroupName</span></span>
<span data-ttu-id="c2b71-122">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="c2b71-122">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c2b71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b71-123">CommonParameters</span></span>
<span data-ttu-id="c2b71-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2b71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b71-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2b71-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b71-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2b71-126">INPUTS</span></span>

### <span data-ttu-id="c2b71-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c2b71-127">None</span></span>

## <span data-ttu-id="c2b71-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2b71-128">OUTPUTS</span></span>

### <span data-ttu-id="c2b71-129">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="c2b71-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="c2b71-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2b71-130">NOTES</span></span>

## <span data-ttu-id="c2b71-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2b71-131">RELATED LINKS</span></span>
