---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245564"
---
# <span data-ttu-id="a3814-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="a3814-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="a3814-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3814-102">SYNOPSIS</span></span>
<span data-ttu-id="a3814-103">Получить или просмотреть контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="a3814-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="a3814-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3814-104">SYNTAX</span></span>

### <span data-ttu-id="a3814-105">ListDevSpacesControllerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3814-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3814-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3814-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3814-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3814-107">DESCRIPTION</span></span>
<span data-ttu-id="a3814-108">Получить или просмотреть контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="a3814-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="a3814-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3814-109">EXAMPLES</span></span>

### <span data-ttu-id="a3814-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3814-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a3814-111">Перечислите все контроллеры в подписке.</span><span class="sxs-lookup"><span data-stu-id="a3814-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="a3814-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a3814-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="a3814-113">Получение контроллеров DevSpaces в подписке.</span><span class="sxs-lookup"><span data-stu-id="a3814-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="a3814-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3814-114">PARAMETERS</span></span>

### <span data-ttu-id="a3814-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3814-115">-DefaultProfile</span></span>
<span data-ttu-id="a3814-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3814-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3814-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3814-117">-Name</span></span>
<span data-ttu-id="a3814-118">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="a3814-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="a3814-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3814-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3814-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3814-120">Resource group name</span></span>

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

### <span data-ttu-id="a3814-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3814-121">CommonParameters</span></span>
<span data-ttu-id="a3814-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3814-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3814-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3814-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3814-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3814-124">INPUTS</span></span>

### <span data-ttu-id="a3814-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="a3814-125">None</span></span>

## <span data-ttu-id="a3814-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3814-126">OUTPUTS</span></span>

### <span data-ttu-id="a3814-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="a3814-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="a3814-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3814-128">NOTES</span></span>

## <span data-ttu-id="a3814-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3814-129">RELATED LINKS</span></span>