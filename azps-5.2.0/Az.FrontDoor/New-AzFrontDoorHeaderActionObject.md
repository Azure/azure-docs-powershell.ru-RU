---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326412"
---
# <span data-ttu-id="01dfd-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="01dfd-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="01dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="01dfd-103">Создание объекта PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="01dfd-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="01dfd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01dfd-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01dfd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="01dfd-106">Создает объект PSHeaderAction для создания объекта PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="01dfd-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="01dfd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="01dfd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01dfd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="01dfd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01dfd-109">PARAMETERS</span></span>

### <span data-ttu-id="01dfd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01dfd-110">-DefaultProfile</span></span>
<span data-ttu-id="01dfd-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01dfd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01dfd-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="01dfd-112">-HeaderActionType</span></span>
<span data-ttu-id="01dfd-113">Какой тип управления нужно применить к заглаву.</span><span class="sxs-lookup"><span data-stu-id="01dfd-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="01dfd-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="01dfd-114">-HeaderName</span></span>
<span data-ttu-id="01dfd-115">Имя заглавного названия, к имени которого будет применяться данное действие.</span><span class="sxs-lookup"><span data-stu-id="01dfd-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="01dfd-116">-Значение</span><span class="sxs-lookup"><span data-stu-id="01dfd-116">-Value</span></span>
<span data-ttu-id="01dfd-117">Значение, с помощью которого нужно обновить заданное имя.</span><span class="sxs-lookup"><span data-stu-id="01dfd-117">The value to update the given header name with.</span></span>
<span data-ttu-id="01dfd-118">Это значение не используется, если actionType — Delete.</span><span class="sxs-lookup"><span data-stu-id="01dfd-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="01dfd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01dfd-119">CommonParameters</span></span>
<span data-ttu-id="01dfd-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01dfd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01dfd-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01dfd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01dfd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01dfd-122">INPUTS</span></span>

### <span data-ttu-id="01dfd-123">Нет</span><span class="sxs-lookup"><span data-stu-id="01dfd-123">None</span></span>

## <span data-ttu-id="01dfd-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01dfd-124">OUTPUTS</span></span>

### <span data-ttu-id="01dfd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="01dfd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="01dfd-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01dfd-126">NOTES</span></span>

## <span data-ttu-id="01dfd-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01dfd-127">RELATED LINKS</span></span>
