---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960760"
---
# <span data-ttu-id="da39b-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="da39b-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="da39b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da39b-102">SYNOPSIS</span></span>
<span data-ttu-id="da39b-103">Получить или перечислить контроллер Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="da39b-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="da39b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da39b-104">SYNTAX</span></span>

### <span data-ttu-id="da39b-105">ListDevSpacesControllerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da39b-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da39b-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="da39b-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da39b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da39b-107">DESCRIPTION</span></span>
<span data-ttu-id="da39b-108">Получить или перечислить контроллер Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="da39b-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="da39b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da39b-109">EXAMPLES</span></span>

### <span data-ttu-id="da39b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da39b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="da39b-111">Перечислить все контроллеры в подписке.</span><span class="sxs-lookup"><span data-stu-id="da39b-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="da39b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="da39b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="da39b-113">Получите контроллеры DevSpaces в подписке.</span><span class="sxs-lookup"><span data-stu-id="da39b-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="da39b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da39b-114">PARAMETERS</span></span>

### <span data-ttu-id="da39b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da39b-115">-DefaultProfile</span></span>
<span data-ttu-id="da39b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da39b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da39b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da39b-117">-Name</span></span>
<span data-ttu-id="da39b-118">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="da39b-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da39b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da39b-119">-ResourceGroupName</span></span>
<span data-ttu-id="da39b-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="da39b-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da39b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da39b-121">CommonParameters</span></span>
<span data-ttu-id="da39b-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da39b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da39b-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da39b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da39b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da39b-124">INPUTS</span></span>

### <span data-ttu-id="da39b-125">Нет</span><span class="sxs-lookup"><span data-stu-id="da39b-125">None</span></span>

## <span data-ttu-id="da39b-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da39b-126">OUTPUTS</span></span>

### <span data-ttu-id="da39b-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="da39b-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="da39b-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da39b-128">NOTES</span></span>

## <span data-ttu-id="da39b-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da39b-129">RELATED LINKS</span></span>
