---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: a6a5b9ed5dbf1faa4a2be345039e53bb3daae291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558144"
---
# <span data-ttu-id="72a4e-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a4e-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="72a4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="72a4e-103">Обновляет конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="72a4e-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72a4e-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72a4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72a4e-105">DESCRIPTION</span></span>
<span data-ttu-id="72a4e-106">Командлет **Set-AzureRmTrafficManagerEndpoint** обновляет конечную точку в диспетчере трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="72a4e-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="72a4e-107">Этот командлет обновляет параметры из локального объекта конечной точки.</span><span class="sxs-lookup"><span data-stu-id="72a4e-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="72a4e-108">Вы можете указать объект конечной точки либо с помощью параметра *TrafficManagerEndpoint* , либо с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="72a4e-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="72a4e-109">Вы можете получить локальный объект, который представляет конечную точку, используя командлет Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="72a4e-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="72a4e-110">Измените объект на локальном компьютере, а затем используйте **Set-AzureRmTrafficManagerEndpoint** , чтобы зафиксировать изменения.</span><span class="sxs-lookup"><span data-stu-id="72a4e-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="72a4e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72a4e-111">EXAMPLES</span></span>

### <span data-ttu-id="72a4e-112">Пример 1: обновление конечной точки</span><span class="sxs-lookup"><span data-stu-id="72a4e-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="72a4e-113">Первая команда получает конечную точку диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="72a4e-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="72a4e-114">Команда хранит конечную точку локально в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="72a4e-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="72a4e-115">Вторая команда изменяет локальную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="72a4e-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="72a4e-116">Эта команда изменяет значение веса конечной точки на 20.</span><span class="sxs-lookup"><span data-stu-id="72a4e-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="72a4e-117">Третья команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="72a4e-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="72a4e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72a4e-118">PARAMETERS</span></span>

### <span data-ttu-id="72a4e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a4e-119">-DefaultProfile</span></span>
<span data-ttu-id="72a4e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72a4e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72a4e-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a4e-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="72a4e-122">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="72a4e-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="72a4e-123">Этот командлет обновляет диспетчер трафика для соответствия этому локальному объекту.</span><span class="sxs-lookup"><span data-stu-id="72a4e-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="72a4e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a4e-124">CommonParameters</span></span>
<span data-ttu-id="72a4e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72a4e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a4e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a4e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a4e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72a4e-127">INPUTS</span></span>

### <span data-ttu-id="72a4e-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a4e-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="72a4e-129">Этот командлет принимает объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="72a4e-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="72a4e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72a4e-130">OUTPUTS</span></span>

### <span data-ttu-id="72a4e-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="72a4e-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="72a4e-132">Этот командлет возвращает объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="72a4e-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="72a4e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="72a4e-133">NOTES</span></span>

## <span data-ttu-id="72a4e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72a4e-134">RELATED LINKS</span></span>
