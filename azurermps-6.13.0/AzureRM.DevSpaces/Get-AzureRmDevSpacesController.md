---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563075"
---
# <span data-ttu-id="77115-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="77115-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="77115-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77115-102">SYNOPSIS</span></span>
<span data-ttu-id="77115-103">Получить или просмотреть контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="77115-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77115-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77115-104">SYNTAX</span></span>

### <span data-ttu-id="77115-105">ListDevSpacesControllerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77115-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77115-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="77115-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77115-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77115-107">DESCRIPTION</span></span>
<span data-ttu-id="77115-108">Получить или просмотреть контроллер DevSpaces Azure.</span><span class="sxs-lookup"><span data-stu-id="77115-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="77115-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77115-109">EXAMPLES</span></span>

### <span data-ttu-id="77115-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77115-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="77115-111">Перечислите все контроллеры в подписке.</span><span class="sxs-lookup"><span data-stu-id="77115-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="77115-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77115-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="77115-113">Получение контроллеров DevSpaces в подписке.</span><span class="sxs-lookup"><span data-stu-id="77115-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="77115-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77115-114">PARAMETERS</span></span>

### <span data-ttu-id="77115-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77115-115">-DefaultProfile</span></span>
<span data-ttu-id="77115-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77115-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77115-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77115-117">-Name</span></span>
<span data-ttu-id="77115-118">Имя контроллера DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="77115-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="77115-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77115-119">-ResourceGroupName</span></span>
<span data-ttu-id="77115-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="77115-120">Resource group name</span></span>

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

### <span data-ttu-id="77115-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77115-121">CommonParameters</span></span>
<span data-ttu-id="77115-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77115-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77115-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77115-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77115-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77115-124">INPUTS</span></span>

### <span data-ttu-id="77115-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="77115-125">None</span></span>

## <span data-ttu-id="77115-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77115-126">OUTPUTS</span></span>

### <span data-ttu-id="77115-127">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="77115-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="77115-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="77115-128">NOTES</span></span>

## <span data-ttu-id="77115-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77115-129">RELATED LINKS</span></span>
