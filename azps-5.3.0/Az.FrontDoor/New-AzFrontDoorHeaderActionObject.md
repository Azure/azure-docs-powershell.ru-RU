---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507430"
---
# <span data-ttu-id="8e9c6-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="8e9c6-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="8e9c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9c6-103">Создание объекта PSHeaderAction.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="8e9c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e9c6-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e9c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e9c6-105">DESCRIPTION</span></span>
<span data-ttu-id="8e9c6-106">Создает объект PSHeaderAction для создания объекта PSRulesEngineAction.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="8e9c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e9c6-107">EXAMPLES</span></span>

### <span data-ttu-id="8e9c6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e9c6-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="8e9c6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e9c6-109">PARAMETERS</span></span>

### <span data-ttu-id="8e9c6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9c6-110">-DefaultProfile</span></span>
<span data-ttu-id="8e9c6-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9c6-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="8e9c6-112">-HeaderActionType</span></span>
<span data-ttu-id="8e9c6-113">Какой тип управления нужно применить к заглавной части.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="8e9c6-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="8e9c6-114">-HeaderName</span></span>
<span data-ttu-id="8e9c6-115">Имя заглавного названия, к имени которого будет применяться данное действие.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="8e9c6-116">-Value</span><span class="sxs-lookup"><span data-stu-id="8e9c6-116">-Value</span></span>
<span data-ttu-id="8e9c6-117">Значение, с помощью которого нужно обновить заданное имя.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-117">The value to update the given header name with.</span></span>
<span data-ttu-id="8e9c6-118">Это значение не используется, если actionType — Delete.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="8e9c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9c6-119">CommonParameters</span></span>
<span data-ttu-id="8e9c6-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9c6-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e9c6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9c6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e9c6-122">INPUTS</span></span>

### <span data-ttu-id="8e9c6-123">Нет</span><span class="sxs-lookup"><span data-stu-id="8e9c6-123">None</span></span>

## <span data-ttu-id="8e9c6-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e9c6-124">OUTPUTS</span></span>

### <span data-ttu-id="8e9c6-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="8e9c6-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="8e9c6-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e9c6-126">NOTES</span></span>

## <span data-ttu-id="8e9c6-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e9c6-127">RELATED LINKS</span></span>
