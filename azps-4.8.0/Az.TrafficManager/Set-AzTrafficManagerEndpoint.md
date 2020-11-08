---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243137"
---
# <span data-ttu-id="987da-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="987da-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="987da-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="987da-102">SYNOPSIS</span></span>
<span data-ttu-id="987da-103">Обновляет конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="987da-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="987da-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="987da-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987da-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="987da-105">DESCRIPTION</span></span>
<span data-ttu-id="987da-106">Командлет **Set-AzTrafficManagerEndpoint** обновляет конечную точку в диспетчере трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="987da-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="987da-107">Этот командлет обновляет параметры из локального объекта конечной точки.</span><span class="sxs-lookup"><span data-stu-id="987da-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="987da-108">Вы можете указать объект конечной точки либо с помощью параметра *TrafficManagerEndpoint* , либо с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="987da-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="987da-109">Вы можете получить локальный объект, который представляет конечную точку, используя командлет Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="987da-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="987da-110">Измените объект на локальном компьютере, а затем используйте **Set-AzTrafficManagerEndpoint** , чтобы зафиксировать изменения.</span><span class="sxs-lookup"><span data-stu-id="987da-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="987da-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="987da-111">EXAMPLES</span></span>

### <span data-ttu-id="987da-112">Пример 1: обновление конечной точки</span><span class="sxs-lookup"><span data-stu-id="987da-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="987da-113">Первая команда получает конечную точку диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="987da-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="987da-114">Команда хранит конечную точку локально в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="987da-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="987da-115">Вторая команда изменяет локальную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="987da-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="987da-116">Эта команда изменяет значение веса конечной точки на 20.</span><span class="sxs-lookup"><span data-stu-id="987da-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="987da-117">Третья команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="987da-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="987da-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="987da-118">PARAMETERS</span></span>

### <span data-ttu-id="987da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987da-119">-DefaultProfile</span></span>
<span data-ttu-id="987da-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="987da-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="987da-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="987da-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="987da-122">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="987da-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="987da-123">Этот командлет обновляет диспетчер трафика для соответствия этому локальному объекту.</span><span class="sxs-lookup"><span data-stu-id="987da-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="987da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987da-124">CommonParameters</span></span>
<span data-ttu-id="987da-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="987da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987da-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987da-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987da-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="987da-127">INPUTS</span></span>

### <span data-ttu-id="987da-128">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="987da-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="987da-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="987da-129">OUTPUTS</span></span>

### <span data-ttu-id="987da-130">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="987da-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="987da-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="987da-131">NOTES</span></span>

## <span data-ttu-id="987da-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="987da-132">RELATED LINKS</span></span>
