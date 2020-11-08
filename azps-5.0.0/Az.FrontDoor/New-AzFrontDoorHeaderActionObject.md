---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247417"
---
# <span data-ttu-id="9f98d-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="9f98d-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="9f98d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f98d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f98d-103">Создать объект PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="9f98d-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="9f98d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f98d-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f98d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f98d-105">DESCRIPTION</span></span>
<span data-ttu-id="9f98d-106">Создает объект PSHeaderAction для создания объекта PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="9f98d-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="9f98d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f98d-107">EXAMPLES</span></span>

### <span data-ttu-id="9f98d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f98d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="9f98d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f98d-109">PARAMETERS</span></span>

### <span data-ttu-id="9f98d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f98d-110">-DefaultProfile</span></span>
<span data-ttu-id="9f98d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f98d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f98d-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="9f98d-112">-HeaderActionType</span></span>
<span data-ttu-id="9f98d-113">Тип манипуляций, применяемых к заголовку.</span><span class="sxs-lookup"><span data-stu-id="9f98d-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f98d-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="9f98d-114">-HeaderName</span></span>
<span data-ttu-id="9f98d-115">Имя верхнего колонтитула, к которому будет применяться это действие.</span><span class="sxs-lookup"><span data-stu-id="9f98d-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="9f98d-116">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="9f98d-116">-Value</span></span>
<span data-ttu-id="9f98d-117">Значение, для которого нужно обновить заданное имя заголовка.</span><span class="sxs-lookup"><span data-stu-id="9f98d-117">The value to update the given header name with.</span></span>
<span data-ttu-id="9f98d-118">Это значение не используется, если параметр удаления.</span><span class="sxs-lookup"><span data-stu-id="9f98d-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="9f98d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f98d-119">CommonParameters</span></span>
<span data-ttu-id="9f98d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f98d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f98d-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f98d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f98d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f98d-122">INPUTS</span></span>

### <span data-ttu-id="9f98d-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="9f98d-123">None</span></span>

## <span data-ttu-id="9f98d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f98d-124">OUTPUTS</span></span>

### <span data-ttu-id="9f98d-125">Microsoft. Azure. Commands. FrontDoor. Models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="9f98d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="9f98d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f98d-126">NOTES</span></span>

## <span data-ttu-id="9f98d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f98d-127">RELATED LINKS</span></span>
