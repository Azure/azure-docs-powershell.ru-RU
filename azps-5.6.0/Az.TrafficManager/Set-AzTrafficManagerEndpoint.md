---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987241"
---
# <span data-ttu-id="dba6b-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dba6b-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="dba6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba6b-102">SYNOPSIS</span></span>
<span data-ttu-id="dba6b-103">Обновляет конечную точку Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="dba6b-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="dba6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dba6b-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba6b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dba6b-105">DESCRIPTION</span></span>
<span data-ttu-id="dba6b-106">Cmdlet **Set-AzTrafficManagerEndpoint** обновляет конечную точку в Диспетчере трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="dba6b-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="dba6b-107">Этот cmdlet обновляет параметры локального объекта конечной точки.</span><span class="sxs-lookup"><span data-stu-id="dba6b-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="dba6b-108">Объект конечной точки можно указать либо с помощью параметра *TrafficManagerEndpoint,* либо с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="dba6b-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="dba6b-109">Локальный объект, который представляет конечную точку, можно получить с помощью Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dba6b-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="dba6b-110">Измените объект локально, а затем зафиксировать изменения с помощью **Set-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="dba6b-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="dba6b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dba6b-111">EXAMPLES</span></span>

### <span data-ttu-id="dba6b-112">Пример 1. Обновление конечной точки</span><span class="sxs-lookup"><span data-stu-id="dba6b-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="dba6b-113">Первая команда получает конечную точку Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="dba6b-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="dba6b-114">Конечная точка хранится локально в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dba6b-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="dba6b-115">Вторая команда изменяет конечную точку локально.</span><span class="sxs-lookup"><span data-stu-id="dba6b-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="dba6b-116">Эта команда изменяет вес конечной точки на 20.</span><span class="sxs-lookup"><span data-stu-id="dba6b-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="dba6b-117">Третья команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dba6b-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="dba6b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dba6b-118">PARAMETERS</span></span>

### <span data-ttu-id="dba6b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba6b-119">-DefaultProfile</span></span>
<span data-ttu-id="dba6b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dba6b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba6b-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dba6b-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="dba6b-122">Определяет локальный **объект TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="dba6b-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="dba6b-123">Этот командлет обновляет диспетчер трафика в связи с этим локальным объектом.</span><span class="sxs-lookup"><span data-stu-id="dba6b-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dba6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba6b-124">CommonParameters</span></span>
<span data-ttu-id="dba6b-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba6b-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba6b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba6b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dba6b-127">INPUTS</span></span>

### <span data-ttu-id="dba6b-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dba6b-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="dba6b-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dba6b-129">OUTPUTS</span></span>

### <span data-ttu-id="dba6b-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dba6b-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="dba6b-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dba6b-131">NOTES</span></span>

## <span data-ttu-id="dba6b-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dba6b-132">RELATED LINKS</span></span>
