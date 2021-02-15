---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238023"
---
# <span data-ttu-id="4b97d-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="4b97d-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="4b97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b97d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b97d-103">Получить или перечислить контроллер Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="4b97d-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="4b97d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b97d-104">SYNTAX</span></span>

### <span data-ttu-id="4b97d-105">ListDevSpacesControllerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b97d-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b97d-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b97d-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b97d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b97d-107">DESCRIPTION</span></span>
<span data-ttu-id="4b97d-108">Получить или перечислить контроллер Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="4b97d-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="4b97d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b97d-109">EXAMPLES</span></span>

### <span data-ttu-id="4b97d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b97d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="4b97d-111">Перечислить все контроллеры в подписке.</span><span class="sxs-lookup"><span data-stu-id="4b97d-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="4b97d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b97d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="4b97d-113">Получите контроллеры DevSpaces в подписке.</span><span class="sxs-lookup"><span data-stu-id="4b97d-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="4b97d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b97d-114">PARAMETERS</span></span>

### <span data-ttu-id="4b97d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b97d-115">-DefaultProfile</span></span>
<span data-ttu-id="4b97d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b97d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b97d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4b97d-117">-Name</span></span>
<span data-ttu-id="4b97d-118">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="4b97d-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="4b97d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b97d-119">-ResourceGroupName</span></span>
<span data-ttu-id="4b97d-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4b97d-120">Resource group name</span></span>

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

### <span data-ttu-id="4b97d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b97d-121">CommonParameters</span></span>
<span data-ttu-id="4b97d-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b97d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b97d-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b97d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b97d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b97d-124">INPUTS</span></span>

### <span data-ttu-id="4b97d-125">Нет</span><span class="sxs-lookup"><span data-stu-id="4b97d-125">None</span></span>

## <span data-ttu-id="4b97d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b97d-126">OUTPUTS</span></span>

### <span data-ttu-id="4b97d-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="4b97d-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4b97d-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b97d-128">NOTES</span></span>

## <span data-ttu-id="4b97d-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b97d-129">RELATED LINKS</span></span>
