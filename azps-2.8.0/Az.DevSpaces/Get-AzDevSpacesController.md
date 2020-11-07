---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 7cc4c61073b0b196faca8d95bd5153abe2587ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721095"
---
# <span data-ttu-id="605b9-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="605b9-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="605b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="605b9-102">SYNOPSIS</span></span>
<span data-ttu-id="605b9-103">Получить или просмотреть контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="605b9-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="605b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="605b9-104">SYNTAX</span></span>

### <span data-ttu-id="605b9-105">ListDevSpacesControllerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="605b9-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="605b9-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="605b9-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="605b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="605b9-107">DESCRIPTION</span></span>
<span data-ttu-id="605b9-108">Получить или просмотреть контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="605b9-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="605b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="605b9-109">EXAMPLES</span></span>

### <span data-ttu-id="605b9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="605b9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="605b9-111">Перечислите все контроллеры в подписке.</span><span class="sxs-lookup"><span data-stu-id="605b9-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="605b9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="605b9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="605b9-113">Получение контроллеров DevSpaces в подписке.</span><span class="sxs-lookup"><span data-stu-id="605b9-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="605b9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="605b9-114">PARAMETERS</span></span>

### <span data-ttu-id="605b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605b9-115">-DefaultProfile</span></span>
<span data-ttu-id="605b9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="605b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605b9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="605b9-117">-Name</span></span>
<span data-ttu-id="605b9-118">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="605b9-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="605b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="605b9-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="605b9-120">Resource group name</span></span>

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

### <span data-ttu-id="605b9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605b9-121">CommonParameters</span></span>
<span data-ttu-id="605b9-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="605b9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605b9-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605b9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605b9-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="605b9-124">INPUTS</span></span>

### <span data-ttu-id="605b9-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="605b9-125">None</span></span>

## <span data-ttu-id="605b9-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="605b9-126">OUTPUTS</span></span>

### <span data-ttu-id="605b9-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="605b9-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="605b9-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="605b9-128">NOTES</span></span>

## <span data-ttu-id="605b9-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="605b9-129">RELATED LINKS</span></span>
