---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243712"
---
# <span data-ttu-id="f412a-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="f412a-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="f412a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f412a-102">SYNOPSIS</span></span>
<span data-ttu-id="f412a-103">Создание объекта в памяти для объекта DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="f412a-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="f412a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f412a-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="f412a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f412a-105">DESCRIPTION</span></span>
<span data-ttu-id="f412a-106">Создание объекта в памяти для объекта DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="f412a-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="f412a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f412a-107">EXAMPLES</span></span>

### <span data-ttu-id="f412a-108">Пример 1. Создание объекта DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="f412a-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="f412a-109">Создание объекта DigitalTwinsIdentity По ИД и расположению</span><span class="sxs-lookup"><span data-stu-id="f412a-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="f412a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f412a-110">PARAMETERS</span></span>

### <span data-ttu-id="f412a-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f412a-111">-EndpointName</span></span>
<span data-ttu-id="f412a-112">Имя ресурса конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f412a-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="f412a-113">-Id</span><span class="sxs-lookup"><span data-stu-id="f412a-113">-Id</span></span>
<span data-ttu-id="f412a-114">Путь удостоверения ресурса.</span><span class="sxs-lookup"><span data-stu-id="f412a-114">Resource identity path.</span></span>

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

### <span data-ttu-id="f412a-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f412a-115">-Location</span></span>
<span data-ttu-id="f412a-116">Расположение DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f412a-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f412a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f412a-117">-ResourceGroupName</span></span>
<span data-ttu-id="f412a-118">Имя группы ресурсов, которая содержит digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f412a-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f412a-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f412a-119">-ResourceName</span></span>
<span data-ttu-id="f412a-120">Имя digitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="f412a-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="f412a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f412a-121">-SubscriptionId</span></span>
<span data-ttu-id="f412a-122">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="f412a-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="f412a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f412a-123">CommonParameters</span></span>
<span data-ttu-id="f412a-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f412a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f412a-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f412a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f412a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f412a-126">INPUTS</span></span>

## <span data-ttu-id="f412a-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f412a-127">OUTPUTS</span></span>

### <span data-ttu-id="f412a-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="f412a-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="f412a-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f412a-129">NOTES</span></span>

<span data-ttu-id="f412a-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f412a-130">ALIASES</span></span>

## <span data-ttu-id="f412a-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f412a-131">RELATED LINKS</span></span>

